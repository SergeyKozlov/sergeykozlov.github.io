# Domain Canonicalization Handoff

**Date:** 2026-11-17  
**Status:** Complete  
**Repository:** `SergeyKozlov/sergeykozlov.github.io`  
**Canonical site:** [https://sergeykozlov.com](https://sergeykozlov.com)

## Goal

Serve the personal website from one GitHub Pages repository, make `.com` the primary public domain, and redirect both `.ru` hostnames to `.com`.

## Final topology

- One GitHub Pages repository: `SergeyKozlov/sergeykozlov.github.io`.
- GitHub Pages custom domain: `sergeykozlov.com`.
- GitHub Pages **Enforce HTTPS** is enabled.
- `sergeykozlov.com` serves the site directly from GitHub Pages.
- `sergeykozlov.ru` and `www.sergeykozlov.ru` return permanent redirects to the corresponding `.com` URL, preserving the path and query string.

## Completed changes

### GitHub Pages

- Changed the repository custom domain from `sergeykozlov.ru` to `sergeykozlov.com`.
- GitHub updated the repository `CNAME` file to `sergeykozlov.com`.
- GitHub reported a successful DNS check, issued the certificate, and allowed HTTPS enforcement; HTTPS enforcement is checked.

### Cloudflare: `sergeykozlov.com`

The zone remains delegated to Cloudflare. Its website records are **DNS only** so GitHub Pages serves the site and certificate directly.

| Type | Name | Value | Proxy |
|---|---|---|---|
| A | `@` | `185.199.108.153` | DNS only |
| A | `@` | `185.199.109.153` | DNS only |
| A | `@` | `185.199.110.153` | DNS only |
| A | `@` | `185.199.111.153` | DNS only |
| CNAME | `www` | `sergeykozlov.github.io` | DNS only |

- Disabled the former Cloudflare redirect rule from `.com` to `.ru`. The disabled rule is retained for rollback reference.
- Cloudflare's separate Universal SSL certificate for this zone is not used for visitor TLS while these records remain DNS only.

### Cloudflare: `sergeykozlov.ru`

- Enabled Cloudflare proxying on the four existing apex A records to GitHub Pages:
  `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, and `185.199.111.153`.
- Updated the existing `www` CNAME to `sergeykozlov.ru` and enabled proxying.
- Created and enabled the single redirect rule **Redirect .ru to .com**:
  - Match host `sergeykozlov.ru` or `www.sergeykozlov.ru`.
  - Return a 301 permanent redirect to `https://sergeykozlov.com` plus the incoming URI path.
  - Preserve the query string.
- Left mail, DKIM, SPF, and other non-website DNS records unchanged.

### Registrar delegation

- At Ru-Center, changed `sergeykozlov.com` nameservers from NIC.RU to:
  - `deb.ns.cloudflare.com`
  - `jihoon.ns.cloudflare.com`
- The `.ru` domain was already delegated to the same Cloudflare nameservers.

## Verification performed

- Public DNS returned the Cloudflare nameservers for `sergeykozlov.com` and the four GitHub Pages A records.
- `https://sergeykozlov.com/` loaded the site over HTTPS.
- GitHub Pages showed the `.com` custom domain, successful DNS check, and checked **Enforce HTTPS**.
- Visiting both `https://sergeykozlov.ru/?verify=1` and `https://www.sergeykozlov.ru/?verify=2` ended at the matching `https://sergeykozlov.com/` URL with the query string intact.

## Rollback notes

To restore `.ru` as the canonical hostname:

1. Disable **Redirect .ru to .com** in the `.ru` Cloudflare zone.
2. Set the GitHub Pages custom domain back to `sergeykozlov.ru` and keep **Enforce HTTPS** enabled after its certificate is ready.
3. Set the `.ru` website A records and `www` CNAME to **DNS only**.
4. Restore the `.com` website records to the needed Cloudflare proxy state and re-enable or recreate the disabled `.com` to `.ru` redirect.
