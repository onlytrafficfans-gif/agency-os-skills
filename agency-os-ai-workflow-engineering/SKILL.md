---
name: agency-os-ai-workflow-engineering
description: Build Agency OS AI assistance, prompts, durable queues, scheduled workflows, classifications, approvals, webhooks, retries, and recovery. Use for automation that must remain evidence-grounded and human-accountable.
---

# Agency OS AI and Workflow Engineering

Use AI to assist research, classification, audits, and writing; do not let model output become evidence. Consequential outreach, qualification, contract, payment, or campaign decisions require the approval defined by the active phase.

## AI records

Store task purpose, provider/model, prompt or template version, input evidence references, output, structured validation result, reviewer state, and cost/usage. Require cited source records for factual claims. Treat model failure, refusal, malformed output, and uncertainty as explicit states.

## Durable workflow contract

Persist workflow/run/step state, tenant, scheduled time, attempt, retry category, idempotency key, external action ID, approval, output reference, and error summary. Bound retries, dead-letter terminal work, checkpoint long jobs, and resume safely after application or worker restarts.

Protect webhook endpoints with provider verification, replay defenses, tenant resolution, and event deduplication. Recheck authorization and approval at execution time, not only when work is queued.

Test overlap, crash/restart, duplicate event delivery, stale evidence, revoked permissions, exhausted retries, approval expiry, and partial external success. Observability must reveal progress and cost without exposing prompts containing restricted data or secrets.
