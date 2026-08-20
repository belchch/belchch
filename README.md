**English** | [Русский](README.ru.md)

## Roman Belchenko

Backend and fullstack development. Python / FastAPI and Kotlin / Spring Boot on the
backend, React and Vue 3 on the frontend. Recent work is on LLM-agent systems with
deterministic verification of the output.

[![Telegram](https://img.shields.io/badge/Telegram-@rbelchenko-26A5E4?style=flat-square&logo=telegram&logoColor=white)](https://t.me/rbelchenko)
[![Email](https://img.shields.io/badge/Email-rbelchenko@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:rbelchenko@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Roman%20Belchenko-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/roman-belchenko-4b3101425/)
[![Habr Career](https://img.shields.io/badge/Habr%20Career-belch-65A3BE?style=flat-square)](https://career.habr.com/belch)

17 years in commercial development — from Oracle PL/SQL and Android to Kotlin / Spring,
and most recently LLM-agent systems. Domains: energy, forensic expertise, fintech.
Senior, based in St. Petersburg, open to remote work and relocation.

Full CV — [Habr Career](https://career.habr.com/belch).

---

### Catalog — document workflows with LLM agents

Own product. A local-first application: you describe a document task in chat, refine
the plan, and save it as a reusable skill. A skill runs as an agent, as deterministic
Python, or as a pipeline, and can be attached to another session as a tool.

[![Catalog](https://raw.githubusercontent.com/belchch/catalog/main/docs/assets/catalog-overview.png)](https://github.com/belchch/catalog)

- Result verification is a separate stage: structure, sections, tables, regex, leftover placeholders, plus an optional LLM judge reported apart from the deterministic checks.
- Nested skill calls use a frozen config hash and budgets on depth, LLM calls and wall time.
- Data stays in a plain folder: Markdown results, Obsidian-compatible wiki-links, SQLite as a rebuildable index.
- DOCX, XLSX, PDF, CSV and Markdown on input; Markdown and templated DOCX on output.
- 24 architecture decisions are written down as [ADRs](https://github.com/belchch/catalog/tree/main/docs/adr).

Python 3.11, FastAPI, Pydantic v2, asyncio, SQLite · React 19, TypeScript, Vite, Tailwind

[Repository](https://github.com/belchch/catalog) · [Code showcase](https://github.com/belchch/catalog-showcase) — four self-contained packages with offline tests: agent loop, OpenAI-compatible provider, verification registry, wikilink rewriting.

---

### EPSE — platform for forensic construction expertise

Commercial project. Case management, on-site inspections with photo capture, defect
markup against GOST templates, bill of quantities, estimates, generated DOCX reports.
18 feature modules on the frontend.

- JWT with access / refresh rotation and granular permissions through a custom `PermissionEvaluator` wired into Spring method security.
- DOCX estimate reports via Apache POI: landscape layout, merged cells, groupings and totals.
- File storage through S3 presigned URLs — the backend does not proxy heavy traffic.
- Backend organised by domain rather than by layer; dynamic filters on JPA Specifications.

Kotlin 2.1, Spring Boot 3.4, Spring Security, Spring Data JPA, PostgreSQL, MinIO / S3, Apache POI · Vue 3 (Composition API), TypeScript, Quasar 2, Pinia

[Code showcase](https://github.com/belchch/epse-showcase) — selected fragments, published with the client's consent. Live demo: [77.110.115.239](http://77.110.115.239) (`demo` / `demo`), [Swagger](http://77.110.115.239:8080/swagger-ui.html). Full source available on request.

---

### Stack

- **Backend** — Python 3.11+, FastAPI, Pydantic v2, asyncio, httpx · Kotlin, Spring Boot, Spring Security, Spring Data JPA
- **Frontend** — TypeScript, React 19, Vue 3, Quasar, Vite, Tailwind, Pinia
- **Data and storage** — PostgreSQL, SQLite, MinIO / S3
- **LLM** — function-calling loops, SSE and WebSocket streaming, OpenAI-compatible providers, OpenRouter, z.ai
- **Documents** — python-docx, openpyxl, pypdf, Apache POI, DOCX templating
- **Testing and process** — pytest, Vitest, ruff, ADRs, CI on every PR (lint, typecheck, tests, build)

---

### Contact

Telegram [@rbelchenko](https://t.me/rbelchenko) · [rbelchenko@gmail.com](mailto:rbelchenko@gmail.com) · [LinkedIn](https://www.linkedin.com/in/roman-belchenko-4b3101425/) · [Habr Career](https://career.habr.com/belch)
