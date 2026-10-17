---
name: agency-os-phase-6-client-operations
description: Implement and verify Agency OS Phase 6 tenant-isolated client marketing operations, authorized ad-account ingestion, conversion capture, attribution, routing, monitoring, and reporting. Use only after Phase 5 has passed.
---

# Agency OS Phase 6 — Client Marketing Operations

Require a passed Phase 5 gate. Client-owned source systems remain authoritative; reconcile rather than silently rewriting their data.

## Implement

- Multi-client workspaces with organization/client membership, scoped roles, row-level service checks, and negative cross-tenant tests on every read, write, export, job, webhook, and cache key.
- Least-privilege OAuth connections for client-approved Google Ads and Meta accounts. Preserve account ownership, granted scopes, token health, and revocation state.
- Incremental, restart-safe ingestion of campaigns, spend, goals, budgets, and performance metrics with provider IDs, source timestamps, currency/time-zone context, and reconciliation status.
- Landing-page conversion tracking plus form/call lead capture with consent and PII controls. Route each lead to the correct client CRM with idempotency and a visible failure queue.
- Appointment, qualified-lead, and supported offline-conversion tracking with deduplicated external writes and source-system acknowledgements.
- Campaign optimization tasks, monthly performance reports, customer-level source attribution, and alerts for broken integrations, spend anomalies, or tracking gaps.

Do not automatically publish ads or materially change budgets without explicit client-authorized permissions, a reviewable change set, approval evidence, limits, and rollback/reconciliation behavior. Suggestions are not executed changes.

## Test the gate

Test tenant isolation, revoked tokens, pagination, late-arriving corrections, currency/time-zone boundaries, attribution deduplication, CRM routing failures, offline conversion retry, and report reconciliation.

Phase 6 passes only when a client-approved test advertising account is connected and campaign spend, lead events, appointments, and downstream outcomes accurately reconcile against source systems, with discrepancies reported rather than hidden.

Run `$agency-os-acceptance-auditor` and stop before Phase 7.
