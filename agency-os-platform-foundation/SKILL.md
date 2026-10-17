---
name: agency-os-platform-foundation
description: Establish or review the shared architecture, typed data model, security boundaries, provider abstractions, durable jobs, observability, and tenant isolation for Agency OS. Use for cross-cutting implementation decisions in any Agency OS phase.
---

# Agency OS Platform Foundation

Audit the existing repository first. Prefer Next.js, TypeScript, Tailwind, PostgreSQL with Prisma or an equivalent typed layer, secure framework authentication with RBAC, persistent workers, Vitest-compatible tests, and Playwright when no stable equivalent already exists.

## Boundaries

Keep UI, business rules, provider adapters, database access, and background jobs separate. Browser code must never receive integration secrets. Validate authentication, organization membership, role, tenant ownership, and input at every server boundary rather than relying on hidden UI.

Represent provider capabilities explicitly. An adapter must normalize data without erasing provenance, expose pagination and rate-limit information when available, map provider errors to honest domain errors, and support connection tests. Do not bypass provider restrictions with scraping.

## Data invariants

- Use UUID primary keys, created/updated timestamps, explicit foreign keys, appropriate unique constraints, and indexes matching real filters.
- Every externally sourced record must retain provider, provider record ID, retrieval time, provenance, and verification/confidence state when meaningful.
- Deduplicate companies by provider identity and normalized domain; deduplicate contacts by provider identity plus defensible normalized identifiers. Treat merge decisions as auditable operations.
- Separate licensed persistent data from display-only or short-lived provider data, and encode retention/deletion rules.
- Keep estimated values distinct from verified values and store the basis for computed scores.
- Record material mutations, permission changes, external writes, and merge/suppression actions in append-oriented audit events.

Core domains may include users, organizations, prospects, contacts, sources, provider records, searches, enrichments, scores, qualification signals, notes, activities, suppression, outreach, messages, appointments, opportunities, proposals, contracts, customers, client accounts, ad accounts, campaigns, metrics, conversions, attribution, integrations, usage, jobs, and audit logs. Add entities only when the active phase needs them; avoid speculative schema breadth.

## Durable execution

Use persistent jobs for long-running or retried work. Define job type, tenant, input reference, status, attempt count, run-after time, idempotency key, error category, and timestamps. Bound retries, distinguish retryable from terminal errors, send exhausted work to a recoverable dead-letter state, and make external writes idempotent.

## Operations and security

- Store secrets in managed encrypted storage or server-only environment variables; redact logs and error payloads.
- Enforce least privilege, credential rotation, suppression/deletion, export restrictions, provider terms, and tenant isolation.
- Make paid calls budget-aware and observable by provider, organization, operation, and outcome.
- Provide structured logs, request/job correlation IDs, error tracking, health checks, job metrics, and integration status without leaking secrets.
- Back critical rules with unit tests, data/provider behavior with integration tests, and user-critical paths with Playwright.

For each change, document environment variables by name and purpose, never by secret value. Treat test fixtures as a separate environment and label them in both data and UI.
