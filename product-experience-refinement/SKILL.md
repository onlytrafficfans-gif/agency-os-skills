---
name: product-experience-refinement
description: Improve an existing app's actual task flow, interaction states, and visual coherence while preserving its identity. Use for this feels unfinished, make this product feel premium, simplify the flow, or refine the experience; not a replacement for user research or a full redesign by default.
---
# Product Experience Refinement

Evaluate the product while doing a real task. Attractive screenshots, heuristic ratings, and code cleanliness do not establish usability.

## Establish the experience
Read the user's intent, existing design conventions, relevant components, and actual rendered interface. Identify the user, entry point, task, useful result, and return path. If the only artifact is a screenshot, bound findings to visible evidence; do not claim navigation, responsiveness, accessibility, or task completion were tested.

Preserve the product's established visual identity and working flows. Reuse its design system. If direction is missing, choose a concrete direction based on the task and audience, then implement a representative screen or journey before extending it. Do not force every tool into a landing page, dashboard, card grid, or one aesthetic. User preferences override style defaults.

## Find consequential friction
Walk the primary journey with realistic content. Check whether users can identify the next action, understand required inputs, predict the result, see progress, recognize success, recover from failure, and find their previous work. Unnecessary decisions, duplicate entry, unexplained terminology, and invisible system state often matter more than decoration.

Evaluate relevant first-use, empty, loading, error, permission, long-content, and returning-user states. Distinguish zero data from failed loading. Keep important actions discoverable without hover. Avoid fake counts, testimonials, activity, progress percentages, and simulated generated output.

Inspect visual hierarchy, typography, density, alignment, spacing, contrast, content wrapping, focus behavior, and responsive layout in the rendered product. Check keyboard use and semantic controls where applicable. Use project-specific accessibility requirements and current authoritative documentation when needed. Never claim WCAG conformance from a small visual inspection.

Motion should explain state or preserve orientation; respect reduced motion. Design waiting behavior around measured or honest unknown latency. Prevent accidental repeated expensive actions where relevant. Confirm destructive consequences and provide recovery where the product supports it, without adding gratuitous confirmation dialogs.

## Implement the focused improvement
Prioritize by observed impact: inability to complete the task, data loss or trust failure, recovery friction, repeated effort, then visual inconsistencies. Describe the triggering condition and the practical effect of each material issue. Separate observed defects, heuristic concerns, and aesthetic preferences. Avoid invented numerical quality or conversion scores.

When implementation is requested, fix the highest-impact coherent group within scope rather than stopping at critique. Change the smallest relevant surface, keep copy concrete, and carry the design through necessary states. Do not introduce another component system or dependency to achieve a small visual change.

## Verify the result
Repeat the same task, content, and viewport used to observe the issue. Verify relevant alternate states and neighboring flows. Include before/after evidence when useful; screenshots alone do not prove a functional repair. Label an agent walkthrough as an agent walkthrough, not human usability research. Claim speed or conversion improvement only when actually measured with a stated method.

Conclude with the user-visible improvement, verification, and remaining uncertainty. Use frontend, accessibility, testing, and production skills for their specific mechanics rather than expanding this into a universal launch audit.
