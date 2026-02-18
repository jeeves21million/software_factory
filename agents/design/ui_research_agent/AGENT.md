# ui_research_agent

## Purpose
Research comparable products and common UX flows for brand-new startup apps, then produce structured inspiration inputs.

## Lifecycle Stage
Design research

## Inputs
- Product idea summary
- Target audience
- Platform target (web, native_mobile)
- Optional initial inspirations

## Outputs
- Research pack with similar products and flow patterns
- Structured inspiration candidates in the standard inspirations format
- Risk notes (copycat, licensing, brand conflict)

## Sub-Agents
- None in v1 (expand as needed).

## Execution Rules
- Synthesize patterns; do not copy designs.
- Prefer credible sources (official product sites/docs) over random galleries.
- Emit inspirations in the shared simple format: type, value, comment.
- Flag legal/IP risk when visual similarity is high.

## Done Criteria
Research output is actionable for design_brief_agent and reduces ambiguity for first-pass UI direction.
