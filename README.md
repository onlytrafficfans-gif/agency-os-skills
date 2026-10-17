# Agency OS Skill Suite

This package turns the Agency OS master engineering scope and capability inventory into 30 reusable Codex skills. The suite separates program control, shared engineering rules, acceptance auditing, eight sequential phases, six engineering specialties, and six agency-operator capabilities.

## Start here

Invoke `$agency-os-program-director` against the real project repository. On a new or unverified project, it routes to `$agency-os-phase-1-discovery`, writes the implementation plan, builds only Phase 1, audits the gate, and stops with evidence or blockers.

## Skills

| Skill | Responsibility |
| --- | --- |
| `agency-os-program-director` | Repository audit, phase routing, truth model, and sequential release gates |
| `agency-os-platform-foundation` | Architecture, data invariants, provider boundaries, security, jobs, and observability |
| `agency-os-acceptance-auditor` | Reproducible evidence and PASS/FAIL/BLOCKED/NOT RUN verdicts |
| `agency-os-phase-1-discovery` | Authentication, live Apollo company search, persistence, deduplication, CRM, and CSV fallback |
| `agency-os-phase-2-enrichment` | Decision-makers, contact verification, explainable scoring, review, and export |
| `agency-os-phase-3-opportunity-intelligence` | Evidence-grounded website and advertising opportunity audits |
| `agency-os-phase-4-outreach` | CRM pipeline, approved email outreach, replies, suppression, and appointments |
| `agency-os-phase-5-sales-conversion` | Discovery, proposals, contracts, payments, and onboarding |
| `agency-os-phase-6-client-operations` | Tenant-safe ad operations, conversion capture, attribution, and reconciliation |
| `agency-os-phase-7-automation-portal` | Durable workflows, human approvals, alerts, and client portal |
| `agency-os-phase-8-production-validation` | Security, restore, compliance, monitoring, economics, and real business validation |

## Engineering specialist skills

| Skill | Responsibility |
| --- | --- |
| `agency-os-web-platform-engineering` | Next.js, React, TypeScript, Tailwind, APIs, PostgreSQL, Prisma, and optional Supabase |
| `agency-os-data-provider-engineering` | Apollo and supplementary provider integration, provenance, validation, deduplication, and scoring |
| `agency-os-crm-outreach-engineering` | CRM, stages, email, deliverability, scheduling, proposals, signatures, and payments |
| `agency-os-ai-workflow-engineering` | AI assistance, prompts, queues, webhooks, retries, approvals, and recovery |
| `agency-os-marketing-measurement-engineering` | Website analysis, Google/Meta/GA4 data, conversion tracking, attribution, and reporting |
| `agency-os-production-engineering` | Auth, RBAC, secrets, privacy, testing, CI/CD, deployment, monitoring, recovery, and documentation |

## Agency operator skills

| Skill | Responsibility |
| --- | --- |
| `agency-os-prospect-qualification` | Ideal-customer profile and human sales-ready review |
| `agency-os-offer-design` | Credible $5,000 monthly offer, scope, pricing, proof, and risk boundaries |
| `agency-os-sales-calls` | Discovery, qualification, closing, and attributable CRM notes |
| `agency-os-google-ads-oversight` | Informed Google Ads review and controlled recommendations |
| `agency-os-lead-economics` | Funnel costs, acquisition cost, break-even, margin, and recurring revenue |
| `agency-os-client-success` | Onboarding, reporting, issues, renewals, retention, and secure offboarding |

## Business accountability and product development

These seven companion skills support business decisions and product execution alongside the existing Agency OS program and phase gates. They do not bypass those gates or grant permission for external actions.

| Skill | Responsibility |
| --- | --- |
| `business-boss` | One selected business outcome, one next commitment, evidence checks, blocker resolution, and a saved accountability record |
| `cash-first-product-triage` | Inspect actual product capabilities and buyer evidence before choosing an offer or route to collected cash |
| `buyer-evidence-experiments` | Bounded demand experiments with explicit observations, decision rules, and honest funnel stages |
| `paid-outcome-delivery` | Verify and repair the promise, payment, access, and useful outcome journey |
| `product-development-loop` | Define the user outcome, prove difficult dependencies, build complete usable slices, and verify behavior |
| `product-experience-refinement` | Improve actual task flows, interaction states, and visual coherence while preserving product identity |
| `execution-learning-loop` | Convert observed execution failures into focused workflow corrections and realistic evaluation cases |

Use `$business-boss` when deciding the next business action or reviewing a commitment. Use `$product-development-loop` for substantial feature work and `$product-experience-refinement` when a product feels unfinished. For Agency OS implementation, retain `$agency-os-program-director` as the program and phase authority. Accountability records belong to the project using the skills; this package includes no personal business board, credentials, or automatic reminders.

## Design guarantees

- The first pass cannot silently expand beyond Phase 1.
- No phase passes on UI rendering alone.
- Live provider workflows cannot be substituted by undisclosed mock data.
- Prospect fit, observed signal, expressed interest, and confirmed intent remain distinct.
- External data retains provenance and verification state.
- Paid calls and external writes are budgeted, observable, authorized, and idempotent.
- Later phases require an evidence-backed pass from the preceding phase.

Each skill includes `agents/openai.yaml` metadata and is suitable for automatic discovery. See [CAPABILITY-MATRIX.md](CAPABILITY-MATRIX.md) for a numbered mapping of all 50 capabilities in the supplied inventory. The package contains instructions, not provider credentials or application source code.
