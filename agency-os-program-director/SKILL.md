---
name: agency-os-program-director
description: Route and govern implementation of the eight-phase Agency OS customer-acquisition platform, enforcing sequential phase gates, truthful provider behavior, and evidence-backed completion. Use when planning, starting, resuming, or reviewing the overall Agency OS program.
---

# Agency OS Program Director

Treat the agency as the first real tenant and the acquisition-to-client-delivery cycle as the product. Optimize for usable prospects, reliable data, and sales conversion rather than dashboard breadth.

## Route the work

1. Inspect the repository, its instructions, current Git state, stack, migrations, tests, and existing integrations before proposing changes. Reuse stable infrastructure.
2. Determine the highest phase that has passed its acceptance gate using repository evidence. A rendered screen or claimed completion is not evidence.
3. Select exactly one active phase:
   - Phase 1: `$agency-os-phase-1-discovery`
   - Phase 2: `$agency-os-phase-2-enrichment`
   - Phase 3: `$agency-os-phase-3-opportunity-intelligence`
   - Phase 4: `$agency-os-phase-4-outreach`
   - Phase 5: `$agency-os-phase-5-sales-conversion`
   - Phase 6: `$agency-os-phase-6-client-operations`
   - Phase 7: `$agency-os-phase-7-automation-portal`
   - Phase 8: `$agency-os-phase-8-production-validation`
4. Apply `$agency-os-platform-foundation` for cross-cutting architecture, data, security, and worker decisions.
5. Apply `$agency-os-acceptance-auditor` before declaring the active phase complete.

For focused implementation inside the active phase, load only the relevant specialist skill: `$agency-os-web-platform-engineering`, `$agency-os-data-provider-engineering`, `$agency-os-crm-outreach-engineering`, `$agency-os-ai-workflow-engineering`, `$agency-os-marketing-measurement-engineering`, or `$agency-os-production-engineering`.

For the agency owner's human-operated work, use `$agency-os-prospect-qualification`, `$agency-os-offer-design`, `$agency-os-sales-calls`, `$agency-os-google-ads-oversight`, `$agency-os-lead-economics`, or `$agency-os-client-success`. These support judgment and operating practice; they do not turn consequential business decisions into unattended automation.

## Release gates

- On a new repository or first development pass, write the Phase 1 implementation plan, build Phase 1 only, then stop with test evidence and blockers.
- Never start Phase N+1 until Phase N has an evidence-backed pass. Planned navigation items may be visible but must be disabled and labeled planned.
- When credentials, provider permissions, or external accounts are missing, complete safe local work, expose an honest blocked state, and list the exact live tests that remain. Never replace a blocked live integration with undisclosed fixtures.
- External writes, paid provider calls, outreach, publishing, budget changes, signing, and payment actions require the authorization appropriate to that action. Existing project access is not blanket authorization.

## Truth model

Keep these states distinct in schemas, UI, copy, and reports:

- prospect fit: a business matches targeting criteria;
- observed signal: verifiable public or authorized evidence;
- expressed interest: a recorded response indicating interest;
- confirmed intent: an explicit, attributable buying action.

Never infer active demand merely from discovery. Never fabricate identities, metrics, intent, provider results, or performance.

## Phase handoff

At the end of every phase, produce source changes, migrations, interface/API notes, environment documentation, automated test results, screenshots of real screens, redacted live-integration evidence, limitations, cost implications, and a pass/fail checklist. Stop at the active phase gate and ask the user to authorize the next phase only after the current gate passes.
