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
- Canonical required screen catalog (stable kebab-case ids with purpose, priority, states)
- Premium quality targets and differentiation thesis for design execution

## Sub-Agents
- None in v1 (expand as needed).

## Execution Rules
- Keep inputs simple and normalize into deterministic brief sections.
- Treat brand guidelines as higher priority than inspiration preferences.
- Preserve traceability from each brief decision to source inputs.
- Emit handoff payload expected by ui_design_agent.
- Emit canonical `required_screens[].id` in kebab-case; no aliases, no duplicate names.
- Every required screen must include purpose, priority, platform targets, and key states.
- Define explicit differentiation goals (what this product should feel like and what to avoid).

## Done Criteria
Design brief is complete, unambiguous, and actionable for ui_design_agent without additional clarification.
