---
name: agency-os-phase-4-outreach
description: Implement and verify Agency OS Phase 4 permission-compliant outreach, CRM stages, sending safeguards, replies, suppression, appointments, ownership, tasks, and conversion reporting. Use only after Phase 3 has passed.
---

# Agency OS Phase 4 — Outreach and Appointments

Require a passed Phase 3 gate. Treat external messages as consequential writes and preserve human control, consent, deliverability, and complete activity history.

## Pipeline

Implement auditable transitions for `New → Researched → Qualified → Contacted → Replied → Meeting Booked → Meeting Completed → Proposal Sent → Negotiation → Won/Lost`. Enforce role permissions, transition rules, ownership, tasks, and timestamps without overwriting history.

## Outreach

- Connect only authorized business-email accounts using server-side credentials and least-privilege scopes.
- Generate drafts from verified prospect facts and approved templates. Require manual approval for first contact and reapproval after material edits.
- Before every send, enforce tenant/provider budgets, recipient eligibility, suppression/opt-out, bounce state, throttle, sending window, and idempotency.
- Persist message content/version, sender, recipient, approval, provider ID, attempt, delivery state, and error without leaking secrets.
- Ingest replies and classify them as suggestions; consequential state changes require human confirmation.
- Process opt-outs and hard bounces promptly and atomically so queued follow-ups cannot send afterward.
- Integrate appointment booking, reminders, and CRM activities with deduplication and reconciliation.

Do not automate mass LinkedIn messaging through scraping, browser automation, or unauthorized endpoints.

## Test the gate

Test duplicate send requests, worker retry/restart, late opt-out races, bounce handling, provider webhooks, spoofed webhook rejection, unauthorized approvals, booking duplication, and reporting calculations. A sandbox can validate plumbing, but it does not prove a live pilot.

Phase 4 passes only after an authorized permission-compliant live pilot records actual sends and replies, correctly suppresses opt-outs, and records booked meetings without duplicate entry. Report delivery, response, meeting, and conversion rates with denominators and time windows.

Run `$agency-os-acceptance-auditor` and stop before Phase 5.
