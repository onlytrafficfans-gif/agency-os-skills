---
name: agency-os-marketing-measurement-engineering
description: Build Agency OS conversion tracking, GA4 and ad-platform ingestion, landing-page analysis, campaign reporting, attribution, dashboards, and optimization controls. Use for measurable client marketing operations in Phases 3 and 6.
---

# Agency OS Marketing and Measurement Engineering

Separate public observations from authorized client data. Public ads can show creative activity; they cannot prove spend, ROI, lead volume, or effectiveness.

## Measurement contract

- Define each event, source, identity key, timestamp semantics, consent basis, deduplication rule, and destination before implementation.
- Treat Google Ads, Meta Marketing API, GA4, call/form tracking, CRM, and payment systems as independently reconcilable sources.
- Preserve account, campaign, currency, time zone, attribution window, source timestamp, ingestion time, and correction state.
- Route leads to the correct client tenant and surface failures for recovery.
- Report counts with denominators, date windows, attribution definitions, and freshness; show missing or delayed data rather than synthetic values.

For landing-page optimization, ground recommendations in observed mobile/desktop behavior, technical measurements, CTA/form paths, and authorized conversion data. For paid search/social operations, generate reviewable change proposals with expected rationale and measurement plan. Publishing or material budget changes require explicit client authorization, bounded permissions, and reconciliation.

Test duplicate events, late corrections, consent changes, time-zone/currency boundaries, broken tags, revoked integrations, attribution disagreement, and cross-tenant routing.
