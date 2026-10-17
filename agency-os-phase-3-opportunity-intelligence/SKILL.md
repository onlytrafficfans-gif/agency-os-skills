---
name: agency-os-phase-3-opportunity-intelligence
description: Implement and verify Agency OS Phase 3 evidence-grounded website, conversion, and permitted advertising opportunity audits with source links, fact checks, and a separate opportunity score. Use only after Phase 2 has passed.
---

# Agency OS Phase 3 — Marketing Opportunity Intelligence

Require a passed Phase 2 gate. Analyze why a specific prospect might benefit from marketing services; never present an inference as proof that the prospect wants help.

## Evidence pipeline

- Assess company sites only with allowed fetching/crawling behavior. Record URL, retrieval time, response state, device/viewport, method, and evidence excerpt or artifact.
- Check mobile and desktop landing behavior, basic technical issues, visible calls to action, forms, and conversion-path observations. Separate automated measurements from human judgments.
- Use public advertising sources within their permissions. For Meta, support an authorized lookup or a human-assisted Ad Library review; for Google Places, obey display, attribution, caching, and retention rules.
- Connect private campaign data only when the account owner has authorized access; label it as authorized first-party integration data.
- Store structured findings with claim type, source link, observed fact, possible implication, confidence, and verification status.

## Audit generation

Build a prospect-specific audit that cites its findings and proposes bounded possible improvements. An AI provider may summarize or draft, but every factual assertion must resolve to stored evidence and pass a human fact-check state before outbound use. Keep the marketing-opportunity score separate from the business-fit score and make its factors explainable.

Never infer advertising spend, ROI, lead volume, lost revenue, or campaign effectiveness from public ads alone. Avoid definitive claims when robots rules, authentication, rendering, consent, or provider limits prevent observation.

## Test the gate

Test source failure and staleness, unsupported claims, citation linkage, AI output validation, score reproducibility, retention rules, and reviewer permissions. Phase 3 passes only with ten prospect audits whose specific possible improvements trace to actual sources and contain no invented spend or performance figures.

Run `$agency-os-acceptance-auditor` and stop before Phase 4.
