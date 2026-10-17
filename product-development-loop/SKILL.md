---
name: product-development-loop
description: Carry a substantial app feature or product upgrade from user outcome through a working end-to-end slice and verified experience. Use for build this product, develop this feature, or improve our development process; skip trivial edits and standalone market research.
---
# Product Development Loop

Connect product judgment, implementation, and experience verification. Use the existing specialist skills for their actual domains instead of repeating their full procedures.

## Inspect and define
Confirm the actual checkout, branch, changes, instructions, platform, and runtime. Trace the relevant current journey before editing. Preserve existing user work, product identity, navigation, data, and working functionality unless the user requested a change. Do not infer a rewrite from upgrade language.

Express the outcome as: this user can perform this task, under these constraints, and observe this result. Include the first useful result and the reason someone would return where repeat use matters. Separate supplied requirements, observations, assumptions, and unresolved decisions. Resolve routine choices directly; ask only for decisions that materially affect scope or irreversible work.

Keep the plan proportional: a few lines for a narrow feature; update an existing product brief for broader work. Record the selected journey, acceptance examples, non-goals, data ownership, provider/access dependencies, and how completion will be demonstrated. Avoid a new documentation stack.

## Prove the difficult dependency early
Identify the assumption most likely to force rework: provider capability, data availability, platform constraint, permissions, latency, billing, or an unfamiliar integration. Inspect the implementation and current official documentation as appropriate. Exercise a minimal real path when authorized and feasible before building a broad interface around it. A fake provider response cannot prove the integration. If blocked, complete independent work and clearly bound what is unverified.

## Build complete usable slices
Choose the smallest coherent user task through input, validation, application logic, authorization, persistence where promised, and visible result. A slice may span UI and backend. Horizontal setup is appropriate when it unblocks the next slice and has an observable check. Do not build every screen first and defer integration until the end.

Use existing patterns, components, tokens, and dependencies. Make local reversible decisions without repeated approval. Distinguish a prototype from production behavior and keep test fixtures out of production claims. Prioritize task completion over extra dashboards, settings, abstractions, or speculative features.

Before implementing UI, determine the relevant states: first use, loading, empty, partial result, success, validation failure, provider failure, and permission failure. Support recovery without losing user input where feasible. Use cancellation, duplicate submission protection, drafts, or job status only when warranted by the actual workflow.

For AI features, define the output contract and representative useful/failing examples. Check real output against the user's task, not merely JSON validity. Handle malformed output and provider failure honestly. Measure latency and usage cost when available; label estimates. Do not replace deterministic logic with AI without a reason.

## Verify and refine
Run checks appropriate to the changed risk and repository requirements. Test behavior, data integrity, and boundaries rather than copying implementation into tests. Include browser or device interaction for user-facing claims. Persistence claims require a reload or reconnect check; multi-user access claims require appropriate isolation checks. A screenshot establishes appearance, not functionality.

Inspect the rendered journey at relevant viewport sizes, with realistic content. Check a first-time user path and a consequential recovery path. Fix observed friction, run relevant regressions, and review the final diff. Use specialist code review according to applicable instructions and delegation authorization; do not claim independent review when none occurred.

Deployment and production mutations follow existing explicit authorization. Provide a concrete reviewable result before asking for any missing release approval. Distinguish local, hosted, provider, and device evidence.

## Finish with evidence
Report the behavior delivered, evidence, and material limitation. For substantial ongoing work, update the existing project tracker with the current verified state, next slice, exact checks, and remaining dependency. Do not update global memory without a direct request. Do not call the feature complete while a required acceptance case is unresolved.

When the commercial outcome is in scope, use cash-first-product-triage or paid-outcome-delivery for the buyer and payment handoff. Ordinary development does not require an unsolicited marketing exercise.
