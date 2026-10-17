---
name: agency-os-phase-8-production-validation
description: Harden, deploy, and validate Agency OS Phase 8 security, recovery, compliance, monitoring, funnel economics, profitability, churn, and operational readiness. Use only after Phase 7 has passed.
---

# Agency OS Phase 8 — Production Readiness and Business Validation

Require a passed Phase 7 gate. This phase validates both engineering readiness and the real acquisition-to-delivery business loop; deployment alone is not completion.

## Production readiness

- Perform dependency, secret, authorization, tenant-isolation, input, webhook, and external-write reviews; remediate critical findings and record accepted residual risk.
- Verify backup creation, encrypted retention, documented recovery objectives, and an actual restoration into an isolated environment with integrity checks.
- Review each provider's permissions, terms, data licensing/retention, deletion/export handling, rate limits, and production approval state.
- Deploy the web application and durable workers with structured monitoring, error tracking, job metrics, health checks, credential rotation, and incident alerts.
- Enforce API expenditure limits and billing alerts, and write system documentation plus incident, provider-outage, credential-compromise, data-correction, and restore runbooks.
- Run critical unit, integration, end-to-end, permission, resilience, and recovery tests against a release candidate.

## Business validation

Build funnel analytics from traceable events and explicit definitions. Report counts, denominators, date windows, cohort logic, currency, and inclusion/exclusion rules for acquisition cost, recurring revenue, churn, and client-service profitability.

Validate with real permissioned data that the system finds high-fit businesses, enriches reachable decision-makers, tracks genuine replies and qualified meetings, preserves proposals and conversions, measures outreach time and provider cost, calculates acquisition cost per paying client, and reconciles client delivery outcomes. A list of company names is not an actionable sales pipeline.

## Final gate

Use `$agency-os-acceptance-auditor` to produce separate engineering-readiness and business-validation verdicts. Any untested restoration, critical isolation failure, noncompliant provider path, missing monitoring on a critical workflow, or unvalidated real funnel remains FAIL or BLOCKED. State clearly whether the business goal—five paying clients at $5,000 per month by April 2027—is achieved, in progress, or not evidenced; never infer it from pipeline projections.
