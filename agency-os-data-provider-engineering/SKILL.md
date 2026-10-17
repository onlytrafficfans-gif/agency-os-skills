---
name: agency-os-data-provider-engineering
description: Integrate Agency OS prospect and advertising data providers with provenance, validation, deduplication, scoring, budgets, permissions, and retention controls. Use for Apollo, Google Places, Meta, LinkedIn, or similar provider work.
---

# Agency OS Data and Provider Engineering

Confirm the provider's current authorized API, account entitlements, terms, field licensing, caching/retention rules, quotas, and costs before implementation. Never use scraping to bypass restrictions.

## Adapter contract

Each provider adapter must expose only supported capabilities, use server-held credentials, normalize without discarding raw provider identity, and classify invalid credentials, permission failures, rate limits, budget blocks, empty results, no-match results, and provider outages distinctly. Preserve provider record ID, retrieval time, source, and verification/confidence state.

For Apollo, support organization and people operations only when the account authorizes them. For Google Places and public Meta research, comply with attribution/display and storage rules. For LinkedIn, use only official permitted integrations; do not automate prohibited messaging or browser scraping.

## Data quality

- Validate domain, company, location, contact, and numeric fields without inventing missing values.
- Deduplicate race-safely using provider identity plus defensible normalized identifiers; record merges and conflicts.
- Keep fit, observed signals, expressed interest, and confirmed intent separate.
- Make scoring explainable by persisting factors, weights, evidence, version, and result. Estimated revenue remains estimated.
- Meter paid operations by tenant/provider/action, enforce budgets before calls, and expose usage without secrets.

Contract-test adapters with sanitized fixtures, but require redacted live evidence before declaring a live workflow complete.
