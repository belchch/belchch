[English](README.md) | **Русский**

## Роман Бельченко

Backend и fullstack-разработка. На бэкенде — Python / FastAPI и Kotlin / Spring Boot,
на фронтенде — React и Vue 3. Последняя работа — системы на LLM-агентах с
детерминированной проверкой результата.

[![Telegram](https://img.shields.io/badge/Telegram-@rbelchenko-26A5E4?style=flat-square&logo=telegram&logoColor=white)](https://t.me/rbelchenko)
[![Email](https://img.shields.io/badge/Email-rbelchenko@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:rbelchenko@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Roman%20Belchenko-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/roman-belchenko-4b3101425/)
[![Habr Career](https://img.shields.io/badge/Habr%20Career-belch-65A3BE?style=flat-square)](https://career.habr.com/belch)

10+ лет production-разработки. Домены: электроэнергетика, судебная экспертиза,
финтех. Санкт-Петербург, открыт к удалённой работе.

Полное резюме — [Хабр Карьера](https://career.habr.com/belch).

---

### Catalog — документные процессы на LLM-агентах

Собственный продукт. Локальное приложение: задача по документам описывается в чате,
план уточняется и сохраняется как переиспользуемый навык. Навык выполняется как агент,
как детерминированный Python или как пайплайн и может быть подключён к другой сессии
как инструмент.

[![Catalog](https://raw.githubusercontent.com/belchch/catalog/main/docs/assets/catalog-overview.png)](https://github.com/belchch/catalog)

- Проверка результата вынесена в отдельный этап: структура, разделы, таблицы, регулярные выражения, незаполненные плейсхолдеры, плюс опциональный LLM-судья отдельно от детерминированных проверок.
- Вложенные вызовы навыков работают на замороженном конфиге с лимитами на глубину, число вызовов модели и общее время.
- Данные лежат в обычной папке: результаты в Markdown, wiki-ссылки для Obsidian, SQLite как перестраиваемый индекс.
- На вход DOCX, XLSX, PDF, CSV и Markdown; на выход Markdown и DOCX по шаблону.
- Архитектурные решения зафиксированы в виде [ADR](https://github.com/belchch/catalog/tree/main/docs/adr).

Python 3.11, FastAPI, Pydantic v2, asyncio, SQLite · React 19, TypeScript, Vite, Tailwind

[Репозиторий](https://github.com/belchch/catalog) · [Видеодемо](https://youtu.be/pSu7ZdjWJ6I)

---

### ЭПСЭ — платформа судебной строительно-технической экспертизы

Коммерческий проект. Ведение дел, осмотры с фотофиксацией, разметка дефектов по
шаблонам с привязкой к ГОСТ, ведомость объёмов работ, сметы, генерация DOCX-отчётов.
18 фича-модулей на фронтенде.

- JWT с ротацией access / refresh и гранулярные права через собственный `PermissionEvaluator`, подключённый к method security.
- Сметные DOCX-отчёты через Apache POI: альбомная ориентация, объединение ячеек, группировки и итоги.
- Файловое хранилище через presigned URL — бэкенд не проксирует тяжёлый трафик.
- Бэкенд организован по доменам, а не по слоям; динамические фильтры на JPA Specifications.

Kotlin 2.1, Spring Boot 3.4, Spring Security, Spring Data JPA, PostgreSQL, MinIO / S3, Apache POI · Vue 3 (Composition API), TypeScript, Quasar 2, Pinia

[Витрина кода](https://github.com/belchch/epse-showcase) — отобранные фрагменты, опубликованы с согласия заказчика. Полный код доступен для просмотра на собеседовании.

---

### Стек

- **Backend** — Python 3.11+, FastAPI, Pydantic v2, asyncio, httpx · Kotlin, Spring Boot, Spring Security, Spring Data JPA
- **Frontend** — TypeScript, React 19, Vue 3, Quasar, Vite, Tailwind, Pinia
- **Данные и хранилища** — PostgreSQL, SQLite, MinIO / S3
- **LLM** — циклы function-calling, стриминг через SSE и WebSocket, OpenAI-совместимые провайдеры, OpenRouter, z.ai
- **Документы** — python-docx, openpyxl, pypdf, Apache POI, шаблоны DOCX
- **Тесты и процесс** — pytest, Vitest, ruff, ADR, CI на каждый PR (линт, типы, тесты, сборка)

---

### Контакты

Telegram [@rbelchenko](https://t.me/rbelchenko) · [rbelchenko@gmail.com](mailto:rbelchenko@gmail.com) · [LinkedIn](https://www.linkedin.com/in/roman-belchenko-4b3101425/) · [Хабр Карьера](https://career.habr.com/belch)
