<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# Сделай плейбук для Ansible который будет получать информацию:

1. Тип CPU, количество ядер, и т.п.
2. Количество оперативной памяти.
3. Информацию о дисках, размер и т.п.
Всю собранную информацию записать в файл, в произвольном формате. Записи начинать с названия хоста.
При работе плейбука использовать become и become-user

Ниже пример простого плейбука и шаблона, который собирает факты о CPU, памяти и дисках, а затем записывает их в файл на целевом хосте, начиная каждую запись с имени хоста и используя `become`/`become_user` для выполнения задач.[^1][^2][^3][^4][^5][^6][^7][^8]

## Пример плейбука

Создай файл `gather_hw_info.yml`:

```yaml
---
- name: Gather hardware info and save to file
  hosts: all
  gather_facts: true

  become: true           # включаем привилегии
  become_user: root      # выполняем задачи от root (можно сменить на нужного пользователя)

  vars:
    info_file: /var/tmp/hw_info.txt   # путь к файлу с результатами

  tasks:
    - name: Ensure destination directory exists
    ansible.builtin.file:
      path: "{{ info_file | dirname }}"
      state: directory
      mode: "0755"

    - name: Render hardware info to file
      ansible.builtin.template:
        src: hw_info.j2
        dest: "{{ info_file }}"
        mode: "0644"
      # при необходимости добавь >> через отдельную задачу с shell/lineinfile,
      # если нужно именно дописывать, а не перезаписывать файл

```

Этот плейбук:[^2][^3][^4][^8][^1]

- Использует `gather_facts: true`, чтобы автоматически собрать факты об оборудовании (CPU, память, диски и т.д.).[^3][^4][^9][^10][^1][^2]
- Включает привилегии с помощью `become: true` и задаёт пользователя с `become_user: root`.[^11][^12][^13][^7][^14]
- Использует модуль `template`, чтобы записать данные в файл в произвольном формате.[^5][^6][^15][^8]


## Шаблон Jinja2 для файла

Создай рядом с плейбуком шаблон `hw_info.j2` (формат можешь менять как угодно, здесь пример «человеческого» текста):[^6][^8][^5]

```jinja2
Host: {{ inventory_hostname }}

CPU:
  Model: {{ ansible_facts['processor'][^1] | default('unknown') }}
  Architecture: {{ ansible_facts['architecture'] | default('unknown') }}
  Physical CPUs: {{ ansible_facts['processor_count'] | default('unknown') }}
  Cores per CPU: {{ ansible_facts['processor_cores'] | default('unknown') }}
  VCPUs: {{ ansible_facts['processor_vcpus'] | default('unknown') }}

Memory:
  Total (MB): {{ ansible_facts['memtotal_mb'] | default('unknown') }}
  Free (MB): {{ ansible_facts['memfree_mb'] | default('unknown') }}

Disks / Filesystems:
{% for m in ansible_facts['mounts'] | default([]) %}
  - Mount: {{ m.mount }}
    Device: {{ m.device }}
    Fstype: {{ m.fstype }}
    Size_total (MB): {{ (m.size_total // 1024 // 1024) if m.size_total is defined else 'unknown' }}
    Size_available (MB): {{ (m.size_available // 1024 // 1024) if m.size_available is defined else 'unknown' }}
{% endfor %}

------------------------------------------------------------
```

В этом шаблоне:[^4][^9][^10][^8][^2][^3]

- Используются стандартные факты Ansible: `ansible_facts['processor_*']` и `ansible_facts['architecture']` для CPU.[^9][^10][^2][^3]
- `ansible_facts['memtotal_mb']` и `ansible_facts['memfree_mb']` для информации об ОЗУ.[^10][^2][^3][^9]
- `ansible_facts['mounts']` (или `ansible_mounts` в старом синтаксисе) для вывода информации о файловых системах и их размерах.[^2][^4][^10]
- Каждая запись начинается с `Host: {{ inventory_hostname }}`, как просили.[^1][^10][^2]


## Как запустить

1. Положи `gather_hw_info.yml` и `hw_info.j2` в один каталог.[^8]
2. Убедись, что в инвентори указаны нужные хосты и настроен доступ по SSH.[^10][^1]
3. Запусти:
```bash
ansible-playbook -i inventory.ini gather_hw_info.yml
```

После выполнения на каждом хосте появится файл `/var/tmp/hw_info.txt` с собранной информацией.[^4][^5][^6][^2]

Если нужно, чтобы информация по разным запуском дописывалась в один и тот же файл (append), можно вместо `template` использовать комбинацию `template` в временный файл и затем `shell: cat /tmp/file >> {{ info_file }}`, но это менее идемпотентно.[^15][^5][^6]
<span style="display:none">[^16][^17][^18][^19][^20]</span>

<div align="center">⁂</div>

[^1]: https://docs.ansible.com/projects/ansible/latest/playbook_guide/playbooks_vars_facts.html

[^2]: https://4sysops.com/archives/gather-system-information-with-ansible-facts/

[^3]: https://spacelift.io/blog/ansible-facts

[^4]: https://docs.ansible.com/projects/ansible/latest/collections/ansible/builtin/setup_module.html

[^5]: https://www.ansiblepilot.com/articles/write-a-variable-to-a-file-ansible-module-copy-vs-template/

[^6]: https://www.redhat.com/en/blog/ansibles-copy-template-modules

[^7]: https://docs.ansible.com/projects/ansible/latest/playbook_guide/playbooks_privilege_escalation.html

[^8]: https://docs.ansible.com/ansible/latest/collections/ansible/builtin/template_module.html

[^9]: https://dev.to/harshm03/ansible-facts-complete-guide-for-beginners-1dcp

[^10]: https://labex.io/tutorials/ansible-how-to-gather-host-information-in-ansible-playbooks-415019

[^11]: https://learning-ocean.com/tutorials/ansible/ansible-become/

[^12]: https://spacelift.io/blog/ansible-become

[^13]: https://stackoverflow.com/questions/38290143/difference-between-become-and-become-user-in-ansible

[^14]: https://docs.ansible.com/ansible/latest/collections/ansible/builtin/runas_become.html

[^15]: https://spacelift.io/blog/ansible-copy

[^16]: https://stackoverflow.com/questions/57102717/how-to-gather-facts-about-disks-using-ansible

[^17]: https://www.reddit.com/r/ansible/comments/kfggi6/can_i_somehow_use_ansible_to_get_all_my_servers/

[^18]: https://github.com/dmccuk/ansible_custom_facts

[^19]: https://www.youtube.com/watch?v=dOHOwAiNF68

[^20]: https://www.reddit.com/r/ansible/comments/1f1n2d3/become_user_not_changing_the_user/

