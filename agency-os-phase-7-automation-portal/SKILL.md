---
name: agency-os-phase-7-automation-portal
description: Implement and verify Agency OS Phase 7 durable prospect, sales, AI-assistance, approval, alerting, reporting, and client-portal automation with recovery and role-based permissions. Use only after Phase 6 has passed.
---

# Agency OS Phase 7 — Automation and Client Portal

Require a passed Phase 6 gate. Automate repeatable coordination while keeping consequential communication, qualification, and campaign decisions accountable to humans.

## Workflows

- Schedule searches and permissioned enrichment within provider terms and configured budgets; checkpoint cursors and make runs idempotent.
- Build a prioritized daily sales queue from explicit, inspectable rules and allow manual reprioritization with an audit event.
- Support AI-assisted audit and message drafting from cited evidence. Store model/provider, prompt/template version, source references, output, and review state.
- Automate follow-up tasks, not unapproved outbound sends. Reply classifications are suggestions until a human confirms consequential actions.
- Detect pipeline and campaign anomalies with documented baselines, thresholds, observation windows, severity, evidence, and acknowledgement/resolution states.
- Persist workflow definitions, runs, steps, attempts, idempotency keys, approvals, outputs, and recovery state. Resume safely after application/worker restarts.

## Client portal and approvals

Expose tenant-scoped reports and only those approved actions allowed by the client's role. Add approval queues for outbound messages and campaign changes with immutable request payloads, diffs, requester/approver separation where required, expiry, and execution linkage. Role-based agent/tool permissions must be checked server-side at execution time.

Generate weekly internal business reports from traceable metrics with denominators and date windows. Never fill missing data with synthetic analytics.

## Test the gate

Test scheduler overlap, crash/restart, duplicate delivery, exhausted retry, approval expiry, revoked permissions, cross-tenant access, stale evidence, anomaly false/clear transitions, and client-visible data filtering.

Phase 7 passes only when workflows survive restarts, expose complete run history, retry recoverable failures, dead-letter terminal failures, and avoid duplicate external actions.

Run `$agency-os-acceptance-auditor` and stop before Phase 8.
