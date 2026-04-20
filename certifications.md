---
layout: default
title: Certifications
permalink: /certifications/
description: Professional certifications and badges
---

<style>
.cert-page {
  --card-bg: rgba(255,255,255,0.06);
  --card-border: rgba(255,255,255,0.12);
  --card-border-strong: rgba(255,255,255,0.18);
  --muted: #b8c2cc;
  --text-strong: #f3f6f9;
  --shadow: 0 18px 42px rgba(0,0,0,0.22);
}

.cert-hero {
  margin: 0 0 2rem;
  padding: 1.6rem;
  border: 1px solid var(--card-border);
  border-radius: 20px;
  background: linear-gradient(180deg, rgba(255,255,255,0.08), rgba(255,255,255,0.03));
  box-shadow: var(--shadow);
}

.cert-hero h1 {
  margin: 0 0 0.4rem;
  font-size: 2rem;
  line-height: 1.15;
}

.cert-hero p {
  margin: 0.35rem 0 0;
  color: var(--muted);
}

.cert-stats {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  gap: 0.8rem;
  margin: 1.2rem 0 0;
}

.cert-stat {
  padding: 0.95rem 1rem;
  border: 1px solid var(--card-border);
  border-radius: 16px;
  background: rgba(255,255,255,0.04);
}

.cert-stat__value {
  display: block;
  font-size: 1.35rem;
  font-weight: 700;
  color: var(--text-strong);
}

.cert-stat__label {
  display: block;
  margin-top: 0.2rem;
  color: var(--muted);
  font-size: 0.92rem;
}

.cert-actions {
  display: flex;
  gap: 0.75rem;
  flex-wrap: wrap;
  margin-top: 1rem;
}

.cert-button,
.cert-link {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  min-height: 40px;
  padding: 0.6rem 0.9rem;
  border-radius: 999px;
  border: 1px solid var(--card-border-strong);
  background: rgba(108,178,255,0.12);
  color: #eef6ff !important;
  text-decoration: none !important;
  font-weight: 600;
  transition: transform 0.15s ease, background 0.15s ease, border-color 0.15s ease;
}

.cert-button:hover,
.cert-link:hover {
  transform: translateY(-1px);
  background: rgba(108,178,255,0.2);
  border-color: rgba(108,178,255,0.45);
}

.cert-toolbar {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 1rem;
  margin: 0 0 1rem;
  padding: 1rem;
  border: 1px solid var(--card-border);
  border-radius: 18px;
  background: rgba(255,255,255,0.04);
}

.cert-field label {
  display: block;
  margin-bottom: 0.45rem;
  color: var(--muted);
  font-size: 0.92rem;
  font-weight: 600;
}

.cert-field select {
  width: 100%;
  min-height: 44px;
  border-radius: 12px;
  border: 1px solid var(--card-border-strong);
  background: rgba(17,24,39,0.75);
  color: #f5f7fa;
  padding: 0.65rem 0.8rem;
}

.cert-toolbar__status {
  display: flex;
  align-items: end;
  color: var(--muted);
  font-size: 0.95rem;
  padding-bottom: 0.35rem;
}

.cert-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 1rem;
}

.cert-card {
  display: grid;
  grid-template-columns: 1fr;
  gap: 1rem;
  padding: 1.15rem;
  border: 1px solid var(--card-border);
  border-radius: 22px;
  background: var(--card-bg);
  box-shadow: var(--shadow);
}

.cert-card.has-embed {
  grid-template-columns: minmax(0, 1fr) 180px;
}

.cert-card__content {
  min-width: 0;
}

.cert-card__head {
  display: flex;
  flex-wrap: wrap;
  gap: 0.55rem;
  margin-bottom: 0.75rem;
}

.cert-chip {
  display: inline-flex;
  align-items: center;
  padding: 0.28rem 0.7rem;
  border-radius: 999px;
  background: rgba(108,178,255,0.14);
  color: #eef6ff;
  font-size: 0.88rem;
  border: 1px solid rgba(108,178,255,0.22);
}

.cert-chip--soft {
  background: rgba(255,255,255,0.06);
  border-color: var(--card-border);
}

.cert-card__title {
  margin: 0 0 0.9rem;
  font-size: 1.35rem;
  line-height: 1.25;
}

.cert-meta {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  gap: 0.7rem;
  margin-bottom: 0.95rem;
}

.cert-meta__item {
  padding: 0.8rem 0.9rem;
  border-radius: 14px;
  border: 1px solid var(--card-border);
  background: rgba(255,255,255,0.03);
}

.cert-meta__label {
  display: block;
  font-size: 0.82rem;
  color: var(--muted);
  margin-bottom: 0.25rem;
}

.cert-meta__value {
  display: block;
  line-height: 1.35;
  color: var(--text-strong);
  word-break: break-word;
}

.cert-card__desc {
  margin: 0 0 1rem;
  color: #dde6ee;
  line-height: 1.65;
}

.cert-links {
  display: flex;
  gap: 0.65rem;
  flex-wrap: wrap;
}

.cert-card__embed {
  min-width: 150px;
  padding: 0.9rem 0.8rem;
  border-radius: 16px;
  border: 1px solid var(--card-border);
  background: rgba(255,255,255,0.03);
  text-align: center;
}

.cert-card__embed-label {
  margin-bottom: 0.75rem;
  color: var(--muted);
  font-size: 0.82rem;
  text-transform: uppercase;
  letter-spacing: 0.08em;
}

.cert-empty {
  display: none;
  margin-top: 1rem;
  padding: 1rem 1.1rem;
  border-radius: 16px;
  border: 1px dashed var(--card-border-strong);
  color: var(--muted);
}

@media (max-width: 860px) {
  .cert-card.has-embed {
    grid-template-columns: 1fr;
  }

  .cert-card__embed {
    justify-self: start;
    width: min(100%, 180px);
  }
}
</style>

<div class="cert-page">
  <section class="cert-hero">
    <h1>Certifications</h1>
    <p>A structured list of professional badges, certificates, issuers, issue dates, expiration data, verification links, and Credly embeds where available.</p>
    <div class="cert-actions">
      <a class="cert-button" href="https://learn.microsoft.com/en-us/users/sergeykozlov/" target="_blank" rel="noopener noreferrer">Microsoft Learn profile</a>
    </div>
    <div class="cert-stats">
      <div class="cert-stat">
        <span class="cert-stat__value">46</span>
        <span class="cert-stat__label">Total certifications</span>
      </div>
      <div class="cert-stat">
        <span class="cert-stat__value">13</span>
        <span class="cert-stat__label">Issuers</span>
      </div>
      <div class="cert-stat">
        <span class="cert-stat__value">40</span>
        <span class="cert-stat__label">Credly embeds</span>
      </div>
    </div>
  </section>

  <section class="cert-toolbar" aria-label="Certification filters">
    <div class="cert-field">
      <label for="issuer-filter">Filter by issuer</label>
      <select id="issuer-filter">
        <option value="all">All issuers</option>
        <option value="Amazon Web Services Training and Certification">Amazon Web Services Training and Certification</option>
        <option value="Certiprof">Certiprof</option>
        <option value="Cisco">Cisco</option>
        <option value="ClickHouse">ClickHouse</option>
        <option value="Cognitive Class">Cognitive Class</option>
        <option value="EC-Council">EC-Council</option>
        <option value="Fortinet">Fortinet</option>
        <option value="IBM">IBM</option>
        <option value="IBM SkillsBuild">IBM SkillsBuild</option>
        <option value="Kaggle">Kaggle</option>
        <option value="Not specified">Not specified</option>
        <option value="The Linux Foundation">The Linux Foundation</option>
        <option value="World Education Services">World Education Services</option>
      </select>
    </div>

    <div class="cert-field">
      <label for="sort-order">Sort by date</label>
      <select id="sort-order">
        <option value="newest">Newest first</option>
        <option value="oldest">Oldest first</option>
        <option value="title">Title A–Z</option>
      </select>
    </div>

    <div class="cert-toolbar__status">
      <span id="results-count">46 items shown</span>
    </div>
  </section>

  <section id="cert-grid" class="cert-grid">
    <article class="cert-card" data-issuer="Kaggle" data-date="" data-title="python">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">Kaggle</span>
<span class="cert-chip cert-chip--soft">—</span>
</div>
<h2 class="cert-card__title">Python</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">Kaggle</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">—</strong></div>
</div>
<div class="cert-links">
<a class="cert-link" href="https://www.kaggle.com/learn/certification/sergeikozlovadmin/python" target="_blank" rel="noopener noreferrer">Kaggle certificate</a>
</div>
</div>
</article>

<article class="cert-card" data-issuer="Kaggle" data-date="" data-title="advanced sql">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">Kaggle</span>
<span class="cert-chip cert-chip--soft">—</span>
</div>
<h2 class="cert-card__title">Advanced SQL</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">Kaggle</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">—</strong></div>
</div>
<div class="cert-links">
<a class="cert-link" href="https://www.kaggle.com/learn/certification/sergeikozlovadmin/advanced-sql" target="_blank" rel="noopener noreferrer">Kaggle certificate</a>
</div>
</div>
</article>

<article class="cert-card has-embed" data-issuer="ClickHouse" data-date="2026-04-17" data-title="clickhouse database professional">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">ClickHouse</span>
<span class="cert-chip cert-chip--soft">2026</span>
</div>
<h2 class="cert-card__title">ClickHouse Database Professional</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">ClickHouse</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">April 17, 2026</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">b965e83c-b91d-4f51-b777-fcb271cec3ae</strong></div>
</div>
<p class="cert-card__desc">Earners of the ClickHouse Database Professional badge can solve real-time analytical problems and build workflows using ClickHouse. In addition to understanding the architecture of how ClickHouse works, earners can define optimized tables, write efficient queries, and optimize the joining of tables. Earners also know how the updating and deleting of data can be done efficiently in ClickHouse using lightweight updates and deletes or the various deduplication table engines.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/b965e83c-b91d-4f51-b777-fcb271cec3ae/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="b965e83c-b91d-4f51-b777-fcb271cec3ae" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="ClickHouse" data-date="2026-04-13" data-title="clickhouse observability professional">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">ClickHouse</span>
<span class="cert-chip cert-chip--soft">2026</span>
</div>
<h2 class="cert-card__title">ClickHouse Observability Professional</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">ClickHouse</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">April 13, 2026</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">1c8a33ff-5281-443b-91f9-b22b6e6b14fd</strong></div>
</div>
<p class="cert-card__desc">Earners of the ClickHouse Observability Professional badge understand ClickHouse internals and how to customize primary keys, partitions, and data types for the observability use case. Earners have practiced data enrichment, schema on read and schema on write with ClickHouse and how to use advanced techniques, such as materialized views and skipping indexes to improve query performance. Finally, earners will know how to set up alerts.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/1c8a33ff-5281-443b-91f9-b22b6e6b14fd/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="1c8a33ff-5281-443b-91f9-b22b6e6b14fd" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="ClickHouse" data-date="2026-04-13" data-title="clickhouse observability associate">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">ClickHouse</span>
<span class="cert-chip cert-chip--soft">2026</span>
</div>
<h2 class="cert-card__title">ClickHouse Observability Associate</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">ClickHouse</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">April 13, 2026</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">057bd52f-1c03-4205-a73c-76ba2e1cdaaa</strong></div>
</div>
<p class="cert-card__desc">Earners of the ClickHouse Observability Associate badge understand the three Observability silos and how ClickHouse, OpenTelemetry, and HyperDX offer the best open-source solution. Earners have practiced ingesting logs, metrics, and application events, explored how to connect different data sources, and learned the basics of querying data using SQL and Lucene syntax in the HyperDX UI.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/057bd52f-1c03-4205-a73c-76ba2e1cdaaa/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="057bd52f-1c03-4205-a73c-76ba2e1cdaaa" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="ClickHouse" data-date="2026-04-12" data-title="chdb professional">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">ClickHouse</span>
<span class="cert-chip cert-chip--soft">2026</span>
</div>
<h2 class="cert-card__title">chDB Professional</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">ClickHouse</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">April 12, 2026</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">e688dbfc-8648-4abc-8e38-88e3dfef6347</strong></div>
</div>
<p class="cert-card__desc">Earners of the ClickHouse chDB Professional badge understand how to use the fast in-process SQL OLAP engine chDB to speed up their analytics or ML workflow. Earners understand how to quickly query from a variety of sources and datatypes with chDB, how to optimize their workflow with chDB, and how to use chDB in their workflow with various chDB integrations.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/e688dbfc-8648-4abc-8e38-88e3dfef6347/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="e688dbfc-8648-4abc-8e38-88e3dfef6347" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="ClickHouse" data-date="2026-04-12" data-title="clickhouse data warehousing professional">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">ClickHouse</span>
<span class="cert-chip cert-chip--soft">2026</span>
</div>
<h2 class="cert-card__title">ClickHouse Data Warehousing Professional</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">ClickHouse</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">April 12, 2026</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">c7f72280-5014-41e3-af75-b6bd8e9d8da9</strong></div>
</div>
<p class="cert-card__desc">Earners of the ClickHouse Data Warehousing Professional badge understand how to ingest, structure, and manage data with ClickHouse. They are able to ingest data both in batches and continuously, and they understand the nuances of updating and deleting data with ClickHouse. Badge earners also know how to efficiently structure data in their ClickHouse data warehouse, and they can use ClickHouse to implement data governance and data quality assurance best practices.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/c7f72280-5014-41e3-af75-b6bd8e9d8da9/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="c7f72280-5014-41e3-af75-b6bd8e9d8da9" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="ClickHouse" data-date="2026-04-12" data-title="clickhouse data warehousing associate">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">ClickHouse</span>
<span class="cert-chip cert-chip--soft">2026</span>
</div>
<h2 class="cert-card__title">ClickHouse Data Warehousing Associate</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">ClickHouse</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">April 12, 2026</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">8180f350-c967-4f94-a86c-a6b13b209a37</strong></div>
</div>
<p class="cert-card__desc">Earners of the ClickHouse Data Warehousing Associate badge understand the fundamentals of ClickHouse architecture, including the foundational differences that make ClickHouse unique like the primary key, primary index, granules and parts. Earners are also able to use ClickHouse as a query engine. They are able to perform ad-hoc analyses using ClickHouse and they can execute queries on external data sources.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/8180f350-c967-4f94-a86c-a6b13b209a37/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="8180f350-c967-4f94-a86c-a6b13b209a37" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="Cisco" data-date="2025-11-24" data-title="apply ai: analyze customer reviews">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">Cisco</span>
<span class="cert-chip cert-chip--soft">2025</span>
</div>
<h2 class="cert-card__title">Apply AI: Analyze Customer Reviews</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">Cisco</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">November 24, 2025</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">5104fa8f-5eac-4763-bacf-68e987f3d2c7</strong></div>
</div>
<p class="cert-card__desc">Cisco verifies the earner of this badge successfully completed the Apply AI: Analyze Customer Reviews Course. The learner has applied thematic analysis to analyze tables of text data with assistance of AI and spreadsheet apps. The learner has practiced choosing the right AI or non-AI tool for each task.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/5104fa8f-5eac-4763-bacf-68e987f3d2c7/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="5104fa8f-5eac-4763-bacf-68e987f3d2c7" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card" data-issuer="Cognitive Class" data-date="2025-09-21" data-title="reactive architecture: distributed messaging platforms">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">Cognitive Class</span>
<span class="cert-chip cert-chip--soft">2025</span>
</div>
<h2 class="cert-card__title">Reactive Architecture: Distributed Messaging Platforms</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">Cognitive Class</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Issued on</span><strong class="cert-meta__value">September 21, 2025</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Note</span><strong class="cert-meta__value">(LB0109EN, provided by Akka)</strong></div>
</div>
<div class="cert-links">
<a class="cert-link" href="https://courses.cognitiveclass.ai/certificates/b27d15b9761b4c6e967b8f2411b7b1de" target="_blank" rel="noopener noreferrer">Cognitive Class certificate</a>
</div>
</div>
</article>

<article class="cert-card has-embed" data-issuer="IBM" data-date="2025-04-11" data-title="data science for business - level 1">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">IBM</span>
<span class="cert-chip cert-chip--soft">2025</span>
</div>
<h2 class="cert-card__title">Data Science for Business - Level 1</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">IBM</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">April 11, 2025</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">8acd062f-133d-439b-820a-3b9d37369a84</strong></div>
</div>
<p class="cert-card__desc">This badge earner understands the relationship between collection and dissemination of data in technology. The individual also understands the public expectation of privacy and the legal and political issues surrounding them.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/8acd062f-133d-439b-820a-3b9d37369a84/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="8acd062f-133d-439b-820a-3b9d37369a84" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="IBM" data-date="2025-04-11" data-title="advanced kubernetes operators">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">IBM</span>
<span class="cert-chip cert-chip--soft">2025</span>
</div>
<h2 class="cert-card__title">Advanced Kubernetes Operators</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">IBM</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">April 11, 2025</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">bb6cebda-08cd-46bc-b180-2002cf16c0a4</strong></div>
</div>
<p class="cert-card__desc">This badge earner has developed advanced skills on building operators with Operator-sdk. They have demonstrated an understanding of the advanced topics of operator control loop reconciliation, deployment and management of operators using Operator Lifecycle Manager, and ways to test deployed operators.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/bb6cebda-08cd-46bc-b180-2002cf16c0a4/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="bb6cebda-08cd-46bc-b180-2002cf16c0a4" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="IBM" data-date="2025-04-07" data-title="intermediate kubernetes operators">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">IBM</span>
<span class="cert-chip cert-chip--soft">2025</span>
</div>
<h2 class="cert-card__title">Intermediate Kubernetes Operators</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">IBM</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">April 07, 2025</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">53672eb5-d2f5-42c4-891f-dfc37b6e491e</strong></div>
</div>
<p class="cert-card__desc">This badge earner has developed skills for building operators with Operator-sdk. They have demonstrated an understanding of the ideas and architecture underlying Kubernetes operators, and successfully constructed and deployed simple Golang, Helm, and Ansible operators.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/53672eb5-d2f5-42c4-891f-dfc37b6e491e/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="53672eb5-d2f5-42c4-891f-dfc37b6e491e" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="IBM" data-date="2025-03-30" data-title="beyond the basics: istio and ibm cloud kubernetes service">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">IBM</span>
<span class="cert-chip cert-chip--soft">2025</span>
</div>
<h2 class="cert-card__title">Beyond the Basics: Istio and IBM Cloud Kubernetes Service</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">IBM</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">March 30, 2025</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">5faf169f-dbbd-4982-aa37-347396671d41</strong></div>
</div>
<p class="cert-card__desc">The badge earner can install Istio in a cluster, deploy a sample app, and set up the Istio Ingress controller. The individual knows how to use metrics, logging and tracing to observe services. The earner is also able to perform simple traffic management such as A/B tests and canary deployments, secure a service mesh, and enforce policies for microservices.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/5faf169f-dbbd-4982-aa37-347396671d41/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="5faf169f-dbbd-4982-aa37-347396671d41" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="Cisco" data-date="2025-03-16" data-title="python essentials 2">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">Cisco</span>
<span class="cert-chip cert-chip--soft">2025</span>
</div>
<h2 class="cert-card__title">Python Essentials 2</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">Cisco</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">March 16, 2025</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">5c53ca12-3098-4ac7-a182-a9663c9af233</strong></div>
</div>
<p class="cert-card__desc">Cisco, in collaboration with OpenEDG Python Institute, verifies the earner of this badge successfully completed the Python Essentials 2 course and achieved the student level credentials. Earners have knowledge and skills in intermediate aspects of Python programming, including modules, packages, exceptions, file processing, as well as general coding techniques and object-oriented programming (OOP), and prepares the learner for the PCAP – Certified Associate in Python Programming certification.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/5c53ca12-3098-4ac7-a182-a9663c9af233/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="5c53ca12-3098-4ac7-a182-a9663c9af233" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="IBM" data-date="2025-02-22" data-title="python for data science">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">IBM</span>
<span class="cert-chip cert-chip--soft">2025</span>
</div>
<h2 class="cert-card__title">Python for Data Science</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">IBM</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">February 22, 2025</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">0fc84102-5b6d-47d9-9333-1ea7d051fb42</strong></div>
</div>
<p class="cert-card__desc">The badge earner is able to write their own Python scripts and perform basic hands-on data analysis using IBM&#x27;s Jupyter-based lab environment.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/0fc84102-5b6d-47d9-9333-1ea7d051fb42/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="0fc84102-5b6d-47d9-9333-1ea7d051fb42" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="Cisco" data-date="2025-01-25" data-title="python essentials 1">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">Cisco</span>
<span class="cert-chip cert-chip--soft">2025</span>
</div>
<h2 class="cert-card__title">Python Essentials 1</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">Cisco</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">January 25, 2025</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">7c9babe2-01f7-4e1f-8b86-4ef7140092d3</strong></div>
</div>
<p class="cert-card__desc">Cisco, in collaboration with OpenEDG Python Institute, verifies the earner of this badge successfully completed the Python Essentials 1 course and achieved the student level credentials. Earners have knowledge of the concepts of computer programming, the syntax and semantics of the Python language as well as demonstrate the ability to accomplish coding tasks related to the essentials of programming in the Python language and resolve implementation challenges using the Python Standard Library.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/7c9babe2-01f7-4e1f-8b86-4ef7140092d3/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="7c9babe2-01f7-4e1f-8b86-4ef7140092d3" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="Cisco" data-date="2025-01-11" data-title="network support and security">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">Cisco</span>
<span class="cert-chip cert-chip--soft">2025</span>
</div>
<h2 class="cert-card__title">Network Support and Security</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">Cisco</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">January 11, 2025</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">1204fa8c-4028-450b-b1cf-a28692a7ac23</strong></div>
</div>
<p class="cert-card__desc">Cisco verifies the earner of this badge successfully completed the Network Support and Security course and achieved this student level credential. Earner has knowledge to support endpoints, networks, and users including diagnostics and documentation as a member of a help desk team as well as an in-depth view of troubleshooting of networks and endpoints and knowledge and skills regarding supporting users and networks remotely. Participated in up to 10 labs and Cisco PT activities.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/1204fa8c-4028-450b-b1cf-a28692a7ac23/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="1204fa8c-4028-450b-b1cf-a28692a7ac23" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="Cisco" data-date="2024-12-31" data-title="english for it 2">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">Cisco</span>
<span class="cert-chip cert-chip--soft">2024</span>
</div>
<h2 class="cert-card__title">English for IT 2</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">Cisco</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">December 31, 2024</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">d8bdc862-228b-446e-9545-e265802e2157</strong></div>
</div>
<p class="cert-card__desc">Cisco, in collaboration with OpenEDG, verifies the earner of this badge successfully completed the English for IT 2 course and achieved the student level credentials. Earners know how to use grammar related to mood, sentence structure and conjunctions; they have an upper-intermediate knowledge of tenses; they can make logical deductions and polite requests, use key phrases related to networking, customer support, software and security engineering, and communicate in English at CEFR B2 level.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/d8bdc862-228b-446e-9545-e265802e2157/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="d8bdc862-228b-446e-9545-e265802e2157" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="IBM" data-date="2024-12-08" data-title="simplifying data pipelines with apache kafka">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">IBM</span>
<span class="cert-chip cert-chip--soft">2024</span>
</div>
<h2 class="cert-card__title">Simplifying Data Pipelines with Apache Kafka</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">IBM</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">December 08, 2024</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">87eee3fa-a5e7-45be-b9c3-259570d34d22</strong></div>
</div>
<p class="cert-card__desc">The badge earner understands the architecture, components and practical application of Kafka for addressing data engineering needs. This includes hands-on demonstration of the essential measures necessary to produce and consume messages using command-line tools, Java APIs, working with Kafka Connect and connecting Kafka to Spark</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/87eee3fa-a5e7-45be-b9c3-259570d34d22/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="87eee3fa-a5e7-45be-b9c3-259570d34d22" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="IBM SkillsBuild" data-date="2024-10-26" data-title="working in a digital world: professional skills">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">IBM SkillsBuild</span>
<span class="cert-chip cert-chip--soft">2024</span>
</div>
<h2 class="cert-card__title">Working in a Digital World: Professional Skills</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">IBM SkillsBuild</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">October 26, 2024</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">4f7e9bde-f014-4354-a40a-c36973325226</strong></div>
</div>
<p class="cert-card__desc">This credential earner understands key skills for professional success and core soft skills needed in the information technology workforce. This includes creating and delivering presentations; using agile approaches for working professionally to deliver quality work and experiences to customers; collaborating effectively with teams; communicating with impact; dealing with challenges in a controlled and focused manner; and solving problems and implementing solutions.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/4f7e9bde-f014-4354-a40a-c36973325226/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="4f7e9bde-f014-4354-a40a-c36973325226" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="Cisco" data-date="2024-10-26" data-title="english for it 1">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">Cisco</span>
<span class="cert-chip cert-chip--soft">2024</span>
</div>
<h2 class="cert-card__title">English for IT 1</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">Cisco</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">October 26, 2024</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">b0ea56f5-9e93-4c64-b72a-858ed08d5215</strong></div>
</div>
<p class="cert-card__desc">Cisco, in collaboration with OpenEDG, verifies the earner of this badge successfully completed the English for IT 1 course and achieved the student level credentials. Earners know how to use complex grammatical concepts correctly; they are familiar with concepts related to information security and job roles, and are able to understand phrases related to customer support; they can use vocabulary related to user experience, fraudulent calls, and network and software engineering.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/b0ea56f5-9e93-4c64-b72a-858ed08d5215/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="b0ea56f5-9e93-4c64-b72a-858ed08d5215" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card" data-issuer="EC-Council" data-date="2024-10-25" data-title="jira agile project management + jira administration + jira agile">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">EC-Council</span>
<span class="cert-chip cert-chip--soft">2024</span>
</div>
<h2 class="cert-card__title">Jira Agile Project Management + Jira Administration + Jira Agile</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">EC-Council</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">October 25, 2024</strong></div>
</div>
<div class="cert-links">
<a class="cert-link" href="https://codered.eccouncil.org/certificate/387ee32b-dc34-439e-86b3-f86925c58532?logged=true" target="_blank" rel="noopener noreferrer">EC-Council certificate</a>
</div>
</div>
</article>

<article class="cert-card" data-issuer="EC-Council" data-date="2024-10-25" data-title="configure juniper srx router using j-web">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">EC-Council</span>
<span class="cert-chip cert-chip--soft">2024</span>
</div>
<h2 class="cert-card__title">Configure Juniper SRX Router Using J-Web</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">EC-Council</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">October 25, 2024</strong></div>
</div>
<div class="cert-links">
<a class="cert-link" href="https://codered.eccouncil.org/certificate/2f40e683-3c15-4003-9cc3-8dfe8130f400?logged=true" target="_blank" rel="noopener noreferrer">EC-Council certificate</a>
</div>
</div>
</article>

<article class="cert-card has-embed" data-issuer="Fortinet" data-date="2024-10-20" data-title="introduction to the threat landscape 2.0">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">Fortinet</span>
<span class="cert-chip cert-chip--soft">2024</span>
</div>
<h2 class="cert-card__title">Introduction to the Threat Landscape 2.0</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">Fortinet</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">October 20, 2024</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">18057159-6555-4d46-a599-587c0db06d5f</strong></div>
</div>
<p class="cert-card__desc">The Introduction to the Threat Landscape 2.0 badge recognizes a fundamental understanding of the cyber threat landscape. The badge earner has demonstrated essential knowledge of the threats that endanger computer networks, the cast of bad actors who are behind cyber threats, and the cyber security principles that can keep users and computer networks safe.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/18057159-6555-4d46-a599-587c0db06d5f/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="18057159-6555-4d46-a599-587c0db06d5f" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="Fortinet" data-date="2024-10-20" data-title="fortinet certified fundamentals cybersecurity">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">Fortinet</span>
<span class="cert-chip cert-chip--soft">2024</span>
</div>
<h2 class="cert-card__title">Fortinet Certified Fundamentals Cybersecurity</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">Fortinet</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">October 20, 2024</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">5ea1ff5f-93f7-4a02-86da-f9bf2a31ced1</strong></div>
</div>
<p class="cert-card__desc">The Fortinet Certified Fundamentals in Cybersecurity certification validates that the earner has mastered the technical skills and knowledge that are required for any entry-level job role in cybersecurity. The curriculum covers today’s threat landscape and the fundamentals of cybersecurity.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/5ea1ff5f-93f7-4a02-86da-f9bf2a31ced1/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="5ea1ff5f-93f7-4a02-86da-f9bf2a31ced1" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="The Linux Foundation" data-date="2024-10-14" data-title="lfel1010: xss exploits and defenses">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">The Linux Foundation</span>
<span class="cert-chip cert-chip--soft">2024</span>
</div>
<h2 class="cert-card__title">LFEL1010: XSS Exploits and Defenses</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">The Linux Foundation</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">October 14, 2024</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">21bc26a3-0550-45dc-9622-ed47052ce3d0</strong></div>
</div>
<p class="cert-card__desc">Earners of the LFEL1010: XSS Exploits and Defenses badge understand the key concepts and practical applications of XSS vulnerabilities. They have hands-on experience identifying, exploiting, and mitigating reflected, stored, and DOM-based XSS using Arduino-based hardware setups.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/21bc26a3-0550-45dc-9622-ed47052ce3d0/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="21bc26a3-0550-45dc-9622-ed47052ce3d0" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="Fortinet" data-date="2024-10-12" data-title="technical introduction to cybersecurity 1.0">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">Fortinet</span>
<span class="cert-chip cert-chip--soft">2024</span>
</div>
<h2 class="cert-card__title">Technical Introduction to Cybersecurity 1.0</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">Fortinet</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">October 12, 2024</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">90419943-5234-4466-9c1c-caeefd033021</strong></div>
</div>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/90419943-5234-4466-9c1c-caeefd033021/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="90419943-5234-4466-9c1c-caeefd033021" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="Certiprof" data-date="2024-10-04" data-title="cybersecurity awareness - capc">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">Certiprof</span>
<span class="cert-chip cert-chip--soft">2024</span>
</div>
<h2 class="cert-card__title">Cybersecurity Awareness - CAPC</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">Certiprof</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">October 04, 2024</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">51d52629-50a0-424f-8fe8-d0334571fd2c</strong></div>
</div>
<p class="cert-card__desc">The holders of this badge have validated and demonstrated a comprehensive understanding of cybersecurity principles and best practices. This badge highlights the individual’s ability to recognize and address common cyber threats, implement effective protective measures, and contribute to a secure digital environment. They understand the importance of cybersecurity and its economic and legal implications.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/51d52629-50a0-424f-8fe8-d0334571fd2c/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
<a class="cert-link" href="https://app.kajabi.com/certificates/a869f766" target="_blank" rel="noopener noreferrer">Kajabi certificate</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="51d52629-50a0-424f-8fe8-d0334571fd2c" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card" data-issuer="Not specified" data-date="2024-10-03" data-title="introduction to itil® v4">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">Not specified</span>
<span class="cert-chip cert-chip--soft">2024</span>
</div>
<h2 class="cert-card__title">Introduction to ITIL® V4</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">Not specified</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">03.10.2024</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Valid for</span><strong class="cert-meta__value">90 days</strong></div>
</div>
<div class="cert-links">
<a class="cert-link" href="https://simpli-web.app.link/e/Fl9xK2TpoNb" target="_blank" rel="noopener noreferrer">Course link</a>
</div>
</div>
</article>

<article class="cert-card has-embed" data-issuer="Certiprof" data-date="2024-10-01" data-title="scrum foundation professional certification - sfpc™">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">Certiprof</span>
<span class="cert-chip cert-chip--soft">2024</span>
</div>
<h2 class="cert-card__title">Scrum Foundation Professional Certification - SFPC™</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">Certiprof</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">October 01, 2024</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Expires on</span><strong class="cert-meta__value">October 01, 2027</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">b34b474c-a26e-4dcc-9965-9721f30a53ff</strong></div>
</div>
<p class="cert-card__desc">Scrum Foundation Professional Certification holders have developed entry-level skills in Scrum that endorse their fundamental knowledge in this framework. They have demonstrated an understanding of the empirical Scrum pillars of transparency, inspection, and adaptation. Their primary focus is on the work of Sprint to make the best possible progress toward these goals.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/b34b474c-a26e-4dcc-9965-9721f30a53ff/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
<a class="cert-link" href="https://certiprof.com/pages/scrum-foundation-professional-certificate-sfpc-en-sp" target="_blank" rel="noopener noreferrer">Certiprof page</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="b34b474c-a26e-4dcc-9965-9721f30a53ff" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="IBM SkillsBuild" data-date="2024-09-18" data-title="enterprise security in practice">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">IBM SkillsBuild</span>
<span class="cert-chip cert-chip--soft">2024</span>
</div>
<h2 class="cert-card__title">Enterprise Security in Practice</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">IBM SkillsBuild</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">September 18, 2024</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">65ab72ae-8273-487f-a69c-9a7b7a6267bc</strong></div>
</div>
<p class="cert-card__desc">This badge earner has completed all the learning activities included in this online learning experience, including hands-on experience, concepts, methods and tools related to the enterprise security domain. The individual has demonstrated skills and understanding in the approaches to elevate an organization’s overall security posture, by adopting practices, methods and tools that increase enterprise cyber resilience.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/65ab72ae-8273-487f-a69c-9a7b7a6267bc/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
<a class="cert-link" href="https://skillsbuild.org/college-students/digital-credentials" target="_blank" rel="noopener noreferrer">SkillsBuild info</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="65ab72ae-8273-487f-a69c-9a7b7a6267bc" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="IBM" data-date="2024-09-04" data-title="containers &amp; kubernetes essentials">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">IBM</span>
<span class="cert-chip cert-chip--soft">2024</span>
</div>
<h2 class="cert-card__title">Containers &amp; Kubernetes Essentials</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">IBM</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">September 04, 2024</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">98bc128c-ea37-4b8a-a333-c8b671401c1c</strong></div>
</div>
<p class="cert-card__desc">This badge earner is able to build and run a container image and understands Kubernetes architecture. They know how to: write a YAML deployment file; expose deployment as a service; manage applications with Kubernetes; use ReplicaSets, auto-scaling, rolling updates and service binding; deploy services; and reap the benefits of OpenShift, Istio and other key tools.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/98bc128c-ea37-4b8a-a333-c8b671401c1c/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
<a class="cert-link" href="https://courses.cognitiveclass.ai/certificates/b77fd79bc6da4e62a7734037e865ebee#" target="_blank" rel="noopener noreferrer">Cognitive Class certificate</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="98bc128c-ea37-4b8a-a333-c8b671401c1c" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="The Linux Foundation" data-date="2024-08-22" data-title="lfel1006: securing projects with openssf scorecard">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">The Linux Foundation</span>
<span class="cert-chip cert-chip--soft">2024</span>
</div>
<h2 class="cert-card__title">LFEL1006: Securing Projects with OpenSSF Scorecard</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">The Linux Foundation</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">August 22, 2024</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">6e9bd9fe-5008-4e95-ba83-92846bf487f3</strong></div>
</div>
<p class="cert-card__desc">Earners of the LFEL1006: Securing Projects with OpenSSF Scorecard badge have demonstrated a working knowledge of OpenSSF Scorecard. They have a strong understanding of how Scorecard can be integrated with any GitHub project, and how to strategically incorporate it to help improve security on any software development lifecycle.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/6e9bd9fe-5008-4e95-ba83-92846bf487f3/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="6e9bd9fe-5008-4e95-ba83-92846bf487f3" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="IBM" data-date="2024-08-19" data-title="ibm cloud essentials">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">IBM</span>
<span class="cert-chip cert-chip--soft">2024</span>
</div>
<h2 class="cert-card__title">IBM Cloud Essentials</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">IBM</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">August 19, 2024</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">df3d9d45-dff7-47cc-b80b-37307be60230</strong></div>
</div>
<p class="cert-card__desc">This badge earner is able to relate how the IBM Cloud enables the different service (IaaS, PaaS, SaaS) models and different deployment (Public, Hybrid, Private) models of cloud computing. They know how to: access the IBM Cloud using various tools and interfaces; discover appropriate IBM Cloud products or services available for specific functionality; articulate the different ways IBM Cloud delivers services to developers and operational teams; and summarize core groups of available services.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/df3d9d45-dff7-47cc-b80b-37307be60230/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="df3d9d45-dff7-47cc-b80b-37307be60230" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="Amazon Web Services Training and Certification" data-date="2024-08-06" data-title="aws knowledge: architecting">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">Amazon Web Services Training and Certification</span>
<span class="cert-chip cert-chip--soft">2024</span>
</div>
<h2 class="cert-card__title">AWS Knowledge: Architecting</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">Amazon Web Services Training and Certification</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">August 06, 2024</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">7b54a75f-a1c2-4f7a-a1c5-d4452818f9f8</strong></div>
</div>
<p class="cert-card__desc">Earners of this badge have developed technical skills and knowledge of AWS concepts and services with a focus on designing solutions on AWS using best practices.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/7b54a75f-a1c2-4f7a-a1c5-d4452818f9f8/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="7b54a75f-a1c2-4f7a-a1c5-d4452818f9f8" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="The Linux Foundation" data-date="2024-08-04" data-title="lfs111: open source and the 5g transition">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">The Linux Foundation</span>
<span class="cert-chip cert-chip--soft">2024</span>
</div>
<h2 class="cert-card__title">LFS111: Open Source and the 5G Transition</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">The Linux Foundation</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">August 04, 2024</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">01dc8be9-d29c-44df-854e-b2003a866fba</strong></div>
</div>
<p class="cert-card__desc">Earners of the LFS111x: Open Source and the 5G Transition badge are equipped to make informed decisions, support initiatives, and contribute to projects that relate to open source networking and emerging technologies. They carry an understanding of the open source ecosystem with discernment on how to support collaboration between open source projects and their own organization, including sustainable implementation through an Open Source Program Office.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/01dc8be9-d29c-44df-854e-b2003a866fba/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="01dc8be9-d29c-44df-854e-b2003a866fba" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="Amazon Web Services Training and Certification" data-date="2024-07-19" data-title="aws knowledge: cloud essentials">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">Amazon Web Services Training and Certification</span>
<span class="cert-chip cert-chip--soft">2024</span>
</div>
<h2 class="cert-card__title">AWS Knowledge: Cloud Essentials</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">Amazon Web Services Training and Certification</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">July 19, 2024</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">5e694540-ba36-4da2-b333-1c68efc87754</strong></div>
</div>
<p class="cert-card__desc">Earners of this badge have developed knowledge of foundational AWS Cloud concepts with a focus on AWS Compute, Storage, Networking and Database services, security, architecture, pricing, and support.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/5e694540-ba36-4da2-b333-1c68efc87754/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="5e694540-ba36-4da2-b333-1c68efc87754" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="Cisco" data-date="2024-07-16" data-title="ethical hacker">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">Cisco</span>
<span class="cert-chip cert-chip--soft">2024</span>
</div>
<h2 class="cert-card__title">Ethical Hacker</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">Cisco</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">July 16, 2024</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">b1969e00-9bf9-44f0-925c-63f48a1335cf</strong></div>
</div>
<p class="cert-card__desc">Cisco verifies the earner of this badge successfully completed the Ethical Hacker course. The holder of this student level credential has a broad understanding of the legal and compliance requirements and is proficient in the art of scoping, executing, reporting vulnerability assessments, and recommending mitigation strategies. The holder has completed up to 34 hands-on activities using Kali Linux, WebSploit, and other tools.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/b1969e00-9bf9-44f0-925c-63f48a1335cf/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="b1969e00-9bf9-44f0-925c-63f48a1335cf" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="The Linux Foundation" data-date="2024-07-15" data-title="lfel1005: security self-assessments for open source projects">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">The Linux Foundation</span>
<span class="cert-chip cert-chip--soft">2024</span>
</div>
<h2 class="cert-card__title">LFEL1005: Security Self-Assessments for Open Source Projects</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">The Linux Foundation</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">July 15, 2024</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">41149394-decc-43bf-8938-212b6d0c341b</strong></div>
</div>
<p class="cert-card__desc">Earners of the LFEL1005: Security Self-Assessment for Open Source Projects badge have worked to create a security self-assessment that will aid their project in planning, joint security assessments, and security audits.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/41149394-decc-43bf-8938-212b6d0c341b/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="41149394-decc-43bf-8938-212b6d0c341b" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="The Linux Foundation" data-date="2024-07-14" data-title="lfel1014: scaling cloud native applications with keda">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">The Linux Foundation</span>
<span class="cert-chip cert-chip--soft">2024</span>
</div>
<h2 class="cert-card__title">LFEL1014: Scaling Cloud Native Applications with KEDA</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">The Linux Foundation</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">July 14, 2024</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">cf3a91f5-16b3-4a91-9b9b-49c5fc2b5deb</strong></div>
</div>
<p class="cert-card__desc">Earners of the LFEL1014: Scaling Cloud Native Applications with KEDA badge demonstrate understanding of Kubernetes autoscaling using KEDA. They can manage and scale cloud native applications in response to real-time events and scale applications with help of built-in scalers.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/cf3a91f5-16b3-4a91-9b9b-49c5fc2b5deb/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="cf3a91f5-16b3-4a91-9b9b-49c5fc2b5deb" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="The Linux Foundation" data-date="2024-07-14" data-title="lfc108: cybersecurity essentials">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">The Linux Foundation</span>
<span class="cert-chip cert-chip--soft">2024</span>
</div>
<h2 class="cert-card__title">LFC108: Cybersecurity Essentials</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">The Linux Foundation</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">July 14, 2024</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">7472a55a-ccd4-4b8d-ae5b-dd42eba4c3c0</strong></div>
</div>
<p class="cert-card__desc">Earners of the LFC108: Cybersecurity Essentials badge can apply security practices and precautions during online activities to minimize risks and securely protect personal and professional information from exposure and compromise. They can also identify what to do if a data breach occurs.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/7472a55a-ccd4-4b8d-ae5b-dd42eba4c3c0/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="7472a55a-ccd4-4b8d-ae5b-dd42eba4c3c0" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="Cisco" data-date="2024-07-13" data-title="network defense">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">Cisco</span>
<span class="cert-chip cert-chip--soft">2024</span>
</div>
<h2 class="cert-card__title">Network Defense</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">Cisco</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">July 13, 2024</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">27f48644-532b-4bfc-98aa-2b4140fe7bed</strong></div>
</div>
<p class="cert-card__desc">Cisco verifies the earner of this badge successfully completed the Network Defense course. The holder of this student-level credential has a broad understanding of techniques to monitor and protect the network, including access control, firewalls, cloud security, and cryptography. They are also familiar with how to evaluate and respond to security alerts.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/27f48644-532b-4bfc-98aa-2b4140fe7bed/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="27f48644-532b-4bfc-98aa-2b4140fe7bed" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="Cisco" data-date="2024-07-09" data-title="endpoint security">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">Cisco</span>
<span class="cert-chip cert-chip--soft">2024</span>
</div>
<h2 class="cert-card__title">Endpoint Security</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">Cisco</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">July 09, 2024</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">7177ed6a-04f3-4289-84e1-751e9706ebe5</strong></div>
</div>
<p class="cert-card__desc">Cisco verifies the earner of this badge successfully completed the Endpoint Security course. The holder of this student-level credential has a broad understanding of basic concepts of network security, as well as operating systems and endpoint security.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/7177ed6a-04f3-4289-84e1-751e9706ebe5/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="7177ed6a-04f3-4289-84e1-751e9706ebe5" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="Cisco" data-date="2024-07-05" data-title="networking basics">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">Cisco</span>
<span class="cert-chip cert-chip--soft">2024</span>
</div>
<h2 class="cert-card__title">Networking Basics</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">Cisco</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">July 05, 2024</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">aae671f4-7c42-4a0d-8ed1-c971a470b7f5</strong></div>
</div>
<p class="cert-card__desc">Cisco verifies the earner of this badge successfully completed the Networking Basics course and achieved this student level credential. Earner has knowledge of the types of networks, how they work, how devices send and receive data, the types of network cabling, how IP addresses find information on the Internet, how transport and applications operate, and has practiced building a home wireless network. Participated in up to 13 Cisco Packet Tracer activities.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/aae671f4-7c42-4a0d-8ed1-c971a470b7f5/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="aae671f4-7c42-4a0d-8ed1-c971a470b7f5" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>

<article class="cert-card has-embed" data-issuer="World Education Services" data-date="2023-10-13" data-title="verified international academic qualifications">
<div class="cert-card__content">
<div class="cert-card__head">
<span class="cert-chip">World Education Services</span>
<span class="cert-chip cert-chip--soft">2023</span>
</div>
<h2 class="cert-card__title">Verified International Academic Qualifications</h2>
<div class="cert-meta">
<div class="cert-meta__item"><span class="cert-meta__label">Issued by</span><strong class="cert-meta__value">World Education Services</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Date issued</span><strong class="cert-meta__value">October 13, 2023</strong></div>
<div class="cert-meta__item"><span class="cert-meta__label">Credly badge ID</span><strong class="cert-meta__value">2d28de4b-b1b2-4a2e-a0f2-2d483700ff59</strong></div>
</div>
<p class="cert-card__desc">This badge: Indicates that World Education Services (WES) has evaluated the associated credential on behalf of the holder. Verifies the authenticity of the claimed credential. Provides assurance that the awarding institution and/or program was accredited at the point that the credential was issued Indicates that the associated credential has been assessed for its Canadian equivalency. Please see the evidence link below which is verification of only the credential with which it is associated.</p>
<div class="cert-links">
<a class="cert-link" href="https://www.credly.com/badges/2d28de4b-b1b2-4a2e-a0f2-2d483700ff59/public_url" target="_blank" rel="noopener noreferrer">Credly badge</a>
</div>
</div>
<aside class="cert-card__embed">
<div class="cert-card__embed-label">Credly embed</div>
<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="2d28de4b-b1b2-4a2e-a0f2-2d483700ff59" data-share-badge-host="https://www.credly.com"></div>
</aside>
</article>
  </section>

  <div id="cert-empty" class="cert-empty">No certificates match the selected issuer.</div>
</div>

<script>
document.addEventListener('DOMContentLoaded', function () {
  const issuerFilter = document.getElementById('issuer-filter');
  const sortOrder = document.getElementById('sort-order');
  const grid = document.getElementById('cert-grid');
  const cards = Array.from(grid.querySelectorAll('.cert-card'));
  const resultsCount = document.getElementById('results-count');
  const emptyState = document.getElementById('cert-empty');

  function compareNewest(a, b) {
    const da = a.dataset.date || '';
    const db = b.dataset.date || '';
    if (da && db) return db.localeCompare(da);
    if (da) return -1;
    if (db) return 1;
    return a.dataset.title.localeCompare(b.dataset.title);
  }

  function compareOldest(a, b) {
    const da = a.dataset.date || '';
    const db = b.dataset.date || '';
    if (da && db) return da.localeCompare(db);
    if (da) return -1;
    if (db) return 1;
    return a.dataset.title.localeCompare(b.dataset.title);
  }

  function compareTitle(a, b) {
    return a.dataset.title.localeCompare(b.dataset.title);
  }

  function applyControls() {
    const issuer = issuerFilter.value;
    const mode = sortOrder.value;

    const visible = cards.filter(function (card) {
      const match = issuer === 'all' || card.dataset.issuer === issuer;
      card.hidden = !match;
      return match;
    });

    const compare = mode === 'oldest' ? compareOldest : mode === 'title' ? compareTitle : compareNewest;
    visible.sort(compare).forEach(function (card) {
      grid.appendChild(card);
    });

    resultsCount.textContent = visible.length + ' item' + (visible.length === 1 ? '' : 's') + ' shown';
    emptyState.style.display = visible.length ? 'none' : 'block';
  }

  issuerFilter.addEventListener('change', applyControls);
  sortOrder.addEventListener('change', applyControls);
  applyControls();
});
</script>
<script async src="https://cdn.credly.com/assets/utilities/embed.js"></script>
