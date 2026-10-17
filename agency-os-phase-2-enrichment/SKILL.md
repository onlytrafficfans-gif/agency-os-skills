---
name: agency-os-phase-2-enrichment
description: Implement and verify Agency OS Phase 2 decision-maker enrichment, contact verification, explainable lead qualification, batch jobs, human review, deduplication, and permitted export. Use only after Phase 1 has passed.
---

# Agency OS Phase 2 — Enrichment and Qualification

Refuse to start implementation until Phase 1 has an evidence-backed pass. Extend the saved-prospect domain rather than building a parallel lead store.

## Implement

- Search permitted Apollo people endpoints by selected company domains and configurable title groups such as owner, president, general manager, and marketing director.
- Retrieve only licensed work-contact fields. Preserve provider provenance and mark email/phone as verified, unverified, unavailable, or provider-specific equivalent without upgrading uncertainty.
- Deduplicate contacts within and across companies using provider IDs and defensible normalized identifiers. Preserve merge history and conflicting-source evidence.
- Run selected or batch enrichment as durable, budget-controlled jobs with visible progress, bounded retry, terminal no-match outcomes, and safe resume.
- Compute transparent weighted lead scores from configured factors: industry fit, location, company size, contact availability, estimated commercial capacity, and verified signals. Store factor values, weights, version, total, and source evidence.
- Keep estimated revenue or capacity distinct from verified figures. Never invent a value to complete a score.
- Add filters for score, decision-maker availability, and contact state; enrichment history; manual verification; and an explicit human-review action before `sales-ready`.
- Export only provider- and law-permitted fields with tenant authorization, audit logging, and suppression/deletion enforcement.

Alternative business-source adapters are optional and must follow the same contract, provenance, retention, and truthful-state rules.

## Test the gate

Exercise provider permission and credit failures, genuine no-match, duplicate contacts, concurrent batches, retry/restart, score reproducibility, manual-review authorization, suppression, and export restrictions.

Phase 2 passes only when real Phase 1 prospects are used; 25 selected companies are enriched or have genuine no-match records; available decision-makers and work contacts persist; scores are explainable from non-fabricated evidence; permitted export succeeds; contacts deduplicate correctly; and a controlled test demonstrates at least ten high-fit prospects with usable verified business contact routes. If the threshold is not met, report the measured shortfall as FAIL rather than altering criteria or data.

Run `$agency-os-acceptance-auditor` and stop before Phase 3.
