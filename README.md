# Agency OS Skill Suite

This package turns the Agency OS master engineering scope and capability inventory into 23 reusable Codex skills. The suite separates program control, shared engineering rules, acceptance auditing, eight sequential phases, six engineering specialties, and six agency-operator capabilities.

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

## Design guarantees

- The first pass cannot silently expand beyond Phase 1.
- No phase passes on UI rendering alone.
- Live provider workflows cannot be substituted by undisclosed mock data.
- Prospect fit, observed signal, expressed interest, and confirmed intent remain distinct.
- External data retains provenance and verification state.
- Paid calls and external writes are budgeted, observable, authorized, and idempotent.
- Later phases require an evidence-backed pass from the preceding phase.

Each skill includes `agents/openai.yaml` metadata and is suitable for automatic discovery. See [CAPABILITY-MATRIX.md](CAPABILITY-MATRIX.md) for a numbered mapping of all 50 capabilities in the supplied inventory. The package contains instructions, not provider credentials or application source code.
