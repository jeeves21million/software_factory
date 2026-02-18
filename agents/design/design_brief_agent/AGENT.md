# design_brief_agent

## Purpose
Convert raw product and design context into a clear, structured design brief that guides UI design.

## Lifecycle Stage
Design brief

## Inputs
- Project summary
- Inspirations (links/images/comments)
- Brand pack (guidelines, logos, approved assets)
- Optional constraints (accessibility, platform, legal)

## Outputs
- Structured design brief
- Consolidated inspirations with rationale
- Screen and content priorities for UI design handoff

## Sub-Agents
- None in v1 (expand as needed).

## Execution Rules
- Keep inputs simple and normalize into deterministic brief sections.
- Treat brand guidelines as higher priority than inspiration preferences.
- Preserve traceability from each brief decision to source inputs.
- Emit handoff payload expected by ui_design_agent.

## Done Criteria
Design brief is complete, unambiguous, and actionable for ui_design_agent without additional clarification.
