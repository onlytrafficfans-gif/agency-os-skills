---
name: paid-outcome-delivery
description: Verify the complete promise-to-payment-to-delivery journey of an app or paid pilot and repair its highest-impact break. Use for launch readiness, monetization failures, activation gaps, and whether a product can actually deliver what buyers purchase.
---
# Paid Outcome Delivery

A passing build is one layer of evidence. Establish whether a buyer can receive the purchased outcome in the actual intended environment.

## Trace the promise
Inspect the current offer and product before selecting checks. Map acquisition source, promise, signup, checkout, payment confirmation, entitlement, first useful outcome, repeat use, and support or cancellation where applicable. Skip irrelevant stages for a one-time deliverable. Preserve the product's existing design and scope.

Record the earliest meaningful break and its evidence. Separate code inspection, local functional tests, provider sandbox tests, hosted checks, real payment, and physical device proof. Do not imply a later stage passed from an earlier one.

## Repair the bottleneck
Prefer the smallest authorized change that restores the promised outcome. For billing, distinguish browser success redirects from server-confirmed payment; verify signed provider notifications, replay/idempotency handling, correct customer entitlement, and failure/cancellation behavior as relevant. Follow the platform-specific billing rules using current official documentation. Never test with a real charge or refund without explicit scoped authorization.

For AI products, confirm actual provider execution, valid error behavior, useful output, storage/reload when promised, and measured or explicitly estimated cost per completed outcome. A mock or static response must remain labeled. Missing credentials are a concrete dependency, not a reason to fabricate success.

Test representative first-time buyer and failure paths. Use the existing test suite and appropriate browser/API/device tools. Choose checks based on the changed risk; do not inflate a coverage metric with implementation-mirroring tests. Never weaken authentication, access controls, or secret handling to make a demo pass.

## Establish measurement
Use available operational data to identify the drop-off with a denominator and time window. Add only essential instrumentation within scope; avoid personal data in events. Distinguish pageviews from activation and activation from retention. When usage is absent, report unknown demand rather than inventing a funnel.

For unit economics, show net receipts minus payment fees and variable fulfillment costs, and state whether owner labor and overhead are included. Stress-test usage and support cost with labeled assumptions. Measure costly paths before assuming unlimited plans are viable.

Finish with what changed, the evidence for each verified stage, the remaining limitation, and the next action required to collect or deliver. No revenue claim without transaction evidence. Coordinate with existing billing, security, deployment, and testing skills rather than duplicating their full procedures.
