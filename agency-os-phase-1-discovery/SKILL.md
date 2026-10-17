---
name: agency-os-phase-1-discovery
description: "Plan, implement, and verify Agency OS Phase 1: authenticated live Apollo company discovery, provider configuration, durable prospect saving, deduplication, CRM search, health states, and CSV fallback. Use only for the Phase 1 vertical slice."
---

# Agency OS Phase 1 — Foundation and Business Discovery

Deliver one working path: authenticated user → real Apollo company search → company detail → saved prospect → persistent searchable CRM record. Build only Phase 1; label later modules planned and keep them nonfunctional.

## Start with an audit and plan

Inspect project identity, instructions, dependencies, auth, schema, migrations, routes, environment handling, tests, and deploy target. Then write an implementation plan that maps each Phase 1 acceptance criterion to code and verification. If no repository exists, establish the stack through `$agency-os-platform-foundation` without prebuilding later phases.

## Implement

- Secure sign-in, protected app/API routes, organization-scoped access, and a responsive near-black/deep-blue SaaS shell.
- Server-only Apollo credential configuration, encrypted persistence when stored, connection test, disconnect/invalidation behavior, and sanitized errors.
- A typed Apollo adapter for authorized organization-search/detail capabilities. Search industry, location, employee range, and revenue range only where the account/endpoint supports them.
- Results that show retrieved name, industry, location, domain, estimated size, source, and available metadata. Handle loading, pagination, empty results, permissions, invalid credentials, and rate limits explicitly.
- Search runs/history and usage or credit information when the provider exposes it. Enforce configured budgets before paid calls and log cost-relevant outcomes without secrets.
- Prospect persistence with source attribution, notes, tags, timestamps, and status `New`, `Reviewing`, `Qualified`, or `Rejected`.
- Race-safe deduplication using unique constraints for provider identity and normalized domain, with an idempotent save operation.
- A filterable, sortable, searchable lead table and a company detail page backed by persisted or currently licensed provider data.
- Health/status checks for application, database, and Apollo connectivity. Do not expose secret values or sensitive diagnostics.
- A primary sidebar for Overview, Find Businesses, Prospects, Contacts, Opportunity Intelligence, Pipeline, Outreach, Appointments, Proposals, Clients, Campaigns, Reports, Integrations, and Settings. In Phase 1, activate only the routes supported by Phase 1; mark every later module as planned and do not simulate functionality.
- Deployment instructions, a secret-free environment variable template, and documented API interfaces for the implemented routes and services.

If Apollo cannot be exercised, implement a disclosed CSV import adapter with row-level validation and provenance. Show `CSV import` as the source. Never make fixtures or samples look live.

## Test the gate

Use unit tests for normalization, validation, status transitions, and error mapping; integration tests for auth, adapter contracts, persistence, budgets, and concurrent deduplication; and Playwright for the complete user flow and responsive critical screens.

Phase 1 passes only when evidence shows: authentication; authorized Apollo connection; a live roofing-company search in Las Vegas returning real data or an honest provider state; detail viewing; five actual companies saved and present after reload; a second market searched without code changes; the first search repeated without duplicates; invalid credentials producing a clear error; and no credential leakage in browser responses or logs. A CSV-only build is blocked on live Apollo acceptance, not a full pass.

Stop after the Phase 1 audit from `$agency-os-acceptance-auditor`. Report source, migrations, API contracts, environment template, tests, screenshots, live evidence, limitations, costs, and blockers before proposing Phase 2.
