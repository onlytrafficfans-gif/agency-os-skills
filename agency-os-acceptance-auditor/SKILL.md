---
name: agency-os-acceptance-auditor
description: Verify an Agency OS phase against its acceptance gate with reproducible tests, redacted live-integration evidence, screenshots, limitations, and costs. Use before marking any phase complete or authorizing the next phase.
---

# Agency OS Acceptance Auditor

Audit observable behavior, not implementation claims. Read the active phase skill and build a requirements-to-evidence matrix before assigning status.

## Evidence classes

Accept evidence from automated test output, database queries that demonstrate durable state, provider responses with secrets and restricted personal data redacted, worker/job records, screenshots of actual screens, structured logs, and source/config inspection. Record the command or procedure, environment, time, result, and artifact location.

Classify every acceptance item as:

- **PASS**: reproduced with sufficient evidence;
- **FAIL**: exercised and produced the wrong result;
- **BLOCKED**: cannot be exercised because a named credential, permission, account, external state, or user authorization is missing;
- **NOT RUN**: not yet exercised;
- **NOT APPLICABLE**: only when the phase requirement genuinely does not apply, with rationale.

Do not convert BLOCKED or NOT RUN into PASS. Mock, fixture, or contract tests can validate local behavior but cannot prove a live provider workflow.

## Audit sequence

1. Confirm repository identity, commit/worktree state, environment class, and active phase.
2. Map each acceptance criterion to implementation and a verification method.
3. Run the narrowest meaningful automated suites, then the phase's end-to-end path.
4. Exercise negative paths: invalid credentials, authorization failure, empty results, rate limits, retries, duplicate operations, and forbidden cross-tenant access where relevant.
5. Check browser payloads, source maps, logs, screenshots, and error messages for secret or restricted-data leakage.
6. Verify persistence across reload/restart and idempotency across repeated operations when required.
7. Capture known limitations, provider/licensing constraints, and expected variable/fixed costs.

## Required report

Lead with the gate verdict. Include the matrix, exact evidence, failures and blockers, security/data findings, cost implications, and the smallest next action. List source code, migrations, API specifications, environment documentation, tests, screenshots, and live-integration results. A phase passes only when all mandatory criteria are PASS and no critical security or data-integrity finding remains.
