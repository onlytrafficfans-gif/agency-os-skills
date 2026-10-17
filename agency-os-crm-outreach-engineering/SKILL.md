---
name: agency-os-crm-outreach-engineering
description: Build Agency OS CRM, sales-stage automation, authorized email, deliverability safeguards, webhooks, suppression, scheduling, proposals, signatures, and payments. Use for focused revenue-workflow engineering in Phases 4 and 5.
---

# Agency OS CRM and Outreach Engineering

Preserve an attributable activity timeline from prospect through won/lost and onboarding. State transitions must be permissioned, validated, and append history rather than erase it.

## Messaging and appointments

- Connect only authorized sending accounts and keep credentials server-side.
- Store template/content versions and verified personalization evidence. Require approval for first contact.
- Before send, enforce recipient eligibility, opt-out/suppression, bounce state, throttles, budget, and idempotency.
- Authenticate webhooks, deduplicate events, reconcile provider status, and prevent queued sends after suppression.
- Synchronize appointments and reminders without duplicate CRM activities.

## Conversion workflow

Snapshot sent proposals, scope, prices, fees, ad budgets, assumptions, and validity. Use provider IDs and idempotency for e-signature requests, customers, invoices, subscriptions, and webhooks. Store tokens rather than payment credentials. Test financial/contract integrations in sandbox unless production action is explicitly authorized.

Exercise invalid permissions, duplicate requests, late webhooks, worker retry, opt-out races, failed payment, cancellation, and partial external failure. Sandbox plumbing is not evidence of a live outreach pilot or real payment.
