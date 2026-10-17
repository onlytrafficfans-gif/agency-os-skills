---
name: agency-os-phase-5-sales-conversion
description: Implement and verify Agency OS Phase 5 discovery, qualification, proposals, contracts, payments, subscriptions, onboarding, and won/lost history. Use only after Phase 4 has passed.
---

# Agency OS Phase 5 — Sales Conversion and Contracting

Require a passed Phase 4 gate. Extend each opportunity's immutable activity history through proposal, signature, payment, and onboarding.

## Implement

- Versioned discovery-call questionnaires and qualification/budget checklists with attributable responses.
- A proposal builder based on reusable, versioned service packages that clearly separates monthly agency fee, client-funded advertising budget, optional setup fees, assumptions, exclusions, and validity dates.
- Versioned scope-of-work templates and proposal snapshots so later template edits cannot alter sent documents.
- Authorized e-signature integration with verified webhooks, signer identity/context, provider status reconciliation, and durable contract records.
- Authorized payment integration for customer records, test invoices/payments, subscriptions, renewals, cancellations, failures, and reconciliation. Store provider tokens/IDs rather than raw payment credentials.
- Client onboarding forms and least-privilege requests for client assets or account access; never solicit reusable passwords when delegated access is available.
- Explicit won/lost transitions and structured reasons. Preserve the entire prospect, outreach, meeting, proposal, contract, and payment lineage.

Use idempotency keys for proposal sends, signature requests, customer creation, invoices, subscriptions, and webhook handling. External financial or contractual actions require user authorization and the provider's sandbox/test mode unless the user explicitly authorizes production.

## Test the gate

Test amount/currency calculations, package versioning, stale proposal handling, duplicate webhooks, spoofed signatures, payment failure, cancellation, authorization boundaries, and partial external failure recovery.

Phase 5 passes only when evidence shows a real proposal sent as authorized, an authorized test contract-signing workflow completed, a test invoice/payment created and verified, and the opportunity transitioned into onboarding without losing record history.

Run `$agency-os-acceptance-auditor` and stop before Phase 6.
