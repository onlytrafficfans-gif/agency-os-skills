---
name: agency-os-web-platform-engineering
description: Build or review the Agency OS Next.js, React, TypeScript, Tailwind, PostgreSQL, Prisma, Supabase, REST API, and dashboard foundation. Use for focused web-platform work within the active phase, not for choosing the program phase.
---

# Agency OS Web Platform Engineering

Work within the phase chosen by `$agency-os-program-director`. Audit the repository before changing frameworks; reuse a stable equivalent rather than forcing the preferred stack.

## Engineering contract

- Use strict TypeScript at API, form, provider, and persistence boundaries. Validate untrusted inputs at runtime.
- Keep React components focused on rendering and interaction; place business rules, provider calls, and database access in server-side modules.
- Build accessible responsive UI with keyboard operation, labels, focus states, semantic tables, honest loading/empty/error states, and no invented analytics.
- Design REST-style or equivalent typed interfaces with authentication, tenant authorization, pagination, stable error shapes, request correlation, and explicit idempotency for retried writes.
- Model PostgreSQL through Prisma or the repository's typed equivalent with UUIDs, timestamps, foreign keys, unique constraints, and query-driven indexes. Commit migrations and test forward application.
- Treat Supabase as optional managed infrastructure, not a requirement to replace working Postgres/auth/storage. If used, enforce server-side access and row-level policies with negative tests.

Verify critical logic with unit tests, database/API behavior with integration tests, and user paths with Playwright. Document implemented APIs and environment variable names. A page rendering does not prove its workflow.
