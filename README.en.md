# Vitaly Ostanin

Tech Lead / Senior Backend Developer

telegram: @vytvyt\
email: vitaly.ostanin@gmail.com\
github: https://github.com/VitalyOstanin/

Date of birth: October 24, 1979.\
Location: Saint Petersburg, Russia.\
Not open to relocation.\
Work format: remote preferred, hybrid negotiable.

## Professional positioning
1. Senior Backend Developer (Node.js);
2. Tech Lead.

## Tech stack
- **Primary languages**: TypeScript, JavaScript (Node.js);
- **Secondary languages** (read and modify with AI assistance): Python, Rust;
- **Backend frameworks**: NestJS;
- **Databases**: PostgreSQL, MongoDB;
- **Caching and messaging**: Redis, RabbitMQ, Kafka, NATS, pg-boss;
- **Infrastructure**: Kubernetes (including Yandex Cloud Managed Kubernetes), Docker, Podman, Buildah, Helm, GitLab CI/CD, Harbor, Linux;
- **Observability**: ELK, Grafana, Loki, Sentry;
- **AI/LLM in development**: Anthropic Claude, OpenAI, Qwen, DeepSeek; API integration; own MCP servers;
- **Testing**: unit (Vitest, Jest), integration, E2E (supertest), load (k6).

## Open Source
- [mcp-chrome-debugger-protocol](https://github.com/VitalyOstanin/mcp-chrome-debugger-protocol) — MCP server for Node.js debugging via Chrome DevTools Protocol;
- [youtrack-mcp](https://github.com/VitalyOstanin/youtrack-mcp) — MCP server for YouTrack issue management and reporting;
- [mongodb-mcp](https://github.com/VitalyOstanin/mongodb-mcp) — MCP server for MongoDB with read-only mode and streaming export;
- [postgres-mcp](https://github.com/VitalyOstanin/postgres-mcp) — MCP server for PostgreSQL operations and schema analysis;
- [sentry-mcp](https://github.com/VitalyOstanin/sentry-mcp) — MCP server for Sentry: organizations and projects, issues with filtering and pagination;
- [gitlab-mcp](https://github.com/VitalyOstanin/gitlab-mcp) — MCP server for GitLab: projects, merge requests with diffs and search, tags with SemVer next-release;
- [markdown-org-extract](https://github.com/VitalyOstanin/markdown-org-extract) — Rust tool for organizing Markdown content in Org Mode style;
- [markdown-org-vscode](https://github.com/VitalyOstanin/markdown-org-vscode) — VS Code extension for markdown-org;
- [tg-export](https://github.com/VitalyOstanin/tg-export) — Telegram data exporter to local disk with flexible configuration (Python);
- [claude-dir-settings](https://github.com/VitalyOstanin/claude-dir-settings) — per-directory Claude Code settings: `.claude-dir-settings.yaml` discovered up the directory tree.

## Executive summary
25+ years in IT, 13+ years on Node.js.\
Architecture and development of backend microservices, enterprise systems integration, task and event queues, database design and optimization, high-load services.\
Team leadership, mentoring, development process organization, incident analysis.\
Long-term retention of project context; grounding in business domain (fintech, payments, fiscal receipts, CRM funnels, anti-fraud); solving complex and neglected tasks.\
Integration of AI assistants into development and testing workflows; training teams on practical AI adoption.

## Strengths
- **Neglected tasks and legacy**: I restore system behavior without documentation — from code, logs, database state, and production behavior. I push tasks across multiple iterations to a production-ready state instead of dropping them midway. Example: restoring broken payment processing and conditional 54-FZ receipt issuance (CloudPayments).
- **Complex integrations**: preventive design — retry, idempotency, edge cases, and observability from day one. Example: a batch of new integrations rolled to production (T-Bank, Robokassa, Yandex SmartCaptcha, amoCRM).
- **Architecture**: I design from invariants (immutable ledger, append-only, double-entry); build in transactional consistency and idempotency from day one; separate the hot path from heavy processing; pick the tool to match the task. Example: PostgreSQL-based financial core; a 4-tier caching system with 50–100× RPS growth.
- **Leadership**: I systematize knowledge into a base (foundation: [infostream](https://github.com/VitalyOstanin/infostream)); set up working development, testing, and deployment processes; on hiring, I distinguish people who actually deliver from people who just talk well.
- **AI tooling**: I roll out AI assistants into team workflows; build my own harnesses (Claude Code plugins + public MCP servers); integrate with the corporate stack. Pragmatic approach — engineer's tool, not a replacement for thinking.
- **Project context and fintech domain**: I retain context of a large project over the long haul; I'm well-grounded in payments, 54-FZ fiscal receipts, CRM funnels, and anti-fraud.

## Professional experience

### Contract work (NDA)
1. Period: March 2026 — April 2026 (2 months);
2. Role: Backend Developer;
3. Stack: Node.js, TypeScript, PostgreSQL;
4. Results:
   - **PostgreSQL-based financial core**: designed and implemented core business entities and operations for deposits, accruals, and payouts. The project was not finished, but the core was delivered.

### Finance.Analytics.News LLC
1. Period: June 2024 — February 2026 (1 year 9 months);
2. Industry: Finance;
3. Role: Tech Lead / Senior Backend Developer;
4. Stack: Node.js, TypeScript, NestJS, PostgreSQL, MongoDB, Redis, pg-boss, Kubernetes (Yandex Cloud), GitLab CI/CD, Helm;
5. Key results:
   - **Performance optimization**: 50–100× RPS growth on bottleneck endpoints by designing a 4-tier caching system: in-flight Promise cache (collapsing concurrent identical requests into a single one) → in-memory (LRU/TTL) → Redis → database;
   - **Payment recovery and new integrations**: restored broken payment processing and conditional 54-FZ receipt generation (CloudPayments) — a neglected task inherited from the previous team; rolled out a batch of new external integrations — payment providers (T-Bank, Robokassa), anti-fraud CAPTCHA (Yandex SmartCaptcha), CRM (amoCRM — leads, deals, funnels);
   - **Technical debt reduction**: fully decommissioned 14 services with unmaintainable code, replacing them with 4 new services on a supported stack;
   - **Infrastructure stabilization**: resolved a critical service-cluster connectivity bug in an in-house discovery node, closed a year-long blocker around migrating the discovery node into the shared production cluster;
   - **CI/CD and infrastructure**: deployed an additional environment on Yandex Cloud Managed Kubernetes (~30 legacy Node.js microservices); wrote and ported Helm charts for all services; migrated services from the old GitLab to the new one; built a fast and secure GitLab Runner (unprivileged Podman + Buildah + Harbor); set up build + deploy-to-Kubernetes pipelines; implemented building with an internal library via SSH→HTTPS transport substitution, pinning versions to arbitrary git refs without storing keys in GitLab;
   - **Cost optimization**: offloaded workloads from two additional data centers (DigitalOcean, Hetzner), prepared a plan to drop Cloudflare;
   - **Testing**: built testing infrastructure across all levels — unit (Vitest/Jest), integration, E2E (supertest), load (k6); implemented a production memory-leak debugging mechanism;
   - **AI in the development process**: rolled out AI assistants via API (Claude Code on Sonnet 4, OpenAI Codex on GPT-5, VS Code Cline) for the team; trained backend and frontend engineers on Kubernetes and Node.js debugging inside it; participated in hiring (closed backend and DevOps positions);
   - **Open Source as a byproduct**: built the Node.js debugging MCP server ([mcp-chrome-debugger-protocol](https://github.com/VitalyOstanin/mcp-chrome-debugger-protocol)).

### Digital Technologies and Platforms
1. Period: November 2022 — April 2024 (1 year 6 months);
2. Location: Moscow;
3. Role: Lead Expert;
4. Stack: Node.js, TypeScript;
5. Results:
   - Design and development of new backend service functionality;
   - Support and enhancement of existing services, code review;
   - IT consulting, knowledge sharing, employee training.

### Mati.io
1. Period: November 2020 — February 2022 (1 year 4 months);
2. Role: Software Engineer;
3. Stack: Node.js, RabbitMQ, MongoDB, PostgreSQL, Redis, ELK, Docker;
4. Results:
   - Participated in core system development and solved architectural problems as part of the architecture council;
   - Introduced task queues (RabbitMQ) for background processing;
   - Implemented user verification processes;
   - Analyzed production incidents and improved system resilience.

### EPAM Systems
1. Period: July 2020 — November 2020 (5 months);
2. Role: Lead Software Engineer;
3. Stack: Node.js;
4. Results:
   - Technical analysis and design of Node.js APIs;
   - Prepared data visualization solutions.

### Draewil
1. Period: April 2018 — July 2020 (2 years 4 months);
2. Role: Software Engineer;
3. Stack: Node.js, MongoDB, RabbitMQ, Redis, ELK;
4. Results:
   - Developed and maintained Node.js microservices;
   - Designed MongoDB data structures;
   - Implemented logistics algorithms;
   - Built a background-task system and incident monitoring.

### Sota Systems
1. Period: January 2017 — March 2018 (1 year 3 months);
2. Role: Software Engineer;
3. Stack: Node.js, PostgreSQL, ActiveMQ;
4. Results:
   - Developed and maintained Node.js microservices.

### YuMoney
1. Period: February 2009 — January 2017 (8 years);
2. Industry: Payment systems and web services;
3. Role: Deputy Head of Web Interfaces Department;
4. Stack: Node.js;
5. Results:
   - Developed a Node.js framework;
   - Migrated product teams from the legacy framework;
   - Participated in development process organization.

### ALT Linux
1. Period: January 2007 — February 2009 (2 years 2 months);
2. Role: Software Developer;
3. Results:
   - RPM package maintenance (Jabber server, XML format family);
   - DocBook documentation support.

### Vzlet Group
1. Period: January 2000 — January 2007 (7 years 1 month);
2. Role: Network Administrator;
3. Results:
   - Heterogeneous network configuration;
   - LDAP authentication, Samba, Subversion.

## Education
1. Level: Higher education;
2. Graduation year: 2004;
3. Institution: Saint Petersburg State University of Engineering and Economics "ENGECON", Saint Petersburg;
4. Specialization: Information Systems in Economics and Management.

## Languages
1. Russian — Native;
2. English — B2.

## Core competencies
1. **Backend**: Node.js, TypeScript, NestJS, API design, multi-tier caching (Redis), queues (RabbitMQ, Kafka, NATS, pg-boss);
2. **Databases**: PostgreSQL (including transactional financial workloads), MongoDB;
3. **Infrastructure**: Kubernetes, Docker, Podman, Buildah, Helm, GitLab CI/CD, Harbor, Linux;
4. **Observability**: ELK, Grafana, Loki, Sentry;
5. **Integrations**: payment systems (CloudPayments, T-Bank, Robokassa), Russian 54-FZ fiscal receipts, amoCRM;
6. **AI in development**: AI assistant integration (Anthropic Claude, OpenAI, Qwen, DeepSeek) via APIs; own MCP servers; rolling out AI assistants into team workflows;
7. **Testing**: unit (Vitest, Jest), integration, E2E (supertest), load (k6); production memory-leak debugging;
8. **Soft skills**: team leadership, mentoring, hiring, development and deployment process organization; long-term retention of project context; strong grounding in business domain (fintech, payments, 54-FZ fiscal receipts, CRM funnels, anti-fraud); solving complex and neglected tasks.
