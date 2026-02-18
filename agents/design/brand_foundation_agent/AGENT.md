# brand_foundation_agent

## Purpose
Create a startup-ready brand foundation when no existing company brand assets are available.

## Lifecycle Stage
Design brand foundation

## Inputs
- Project summary
- Target audience
- Platform target
- Optional inspirations and competitor references

## Outputs
- Brand foundation (positioning, voice, visual direction)
- Starter brand pack draft (palette, typography direction, logo brief)
- Handoff payload for design brief creation
- Token system primitives (color roles, typography, spacing, radius, motion)
- Visual territories and anti-patterns to preserve originality

## Sub-Agents
- None in v1 (expand as needed).

## Execution Rules
- Produce original guidance; do not copy other brands.
- Keep outputs explicit and machine-readable where possible.
- Generate practical defaults suitable for first design iteration.
- Include clear "do not do" stylistic constraints to avoid generic outputs.
- Ensure the brand direction is strong enough to drive award-level design differentiation.

## Done Criteria
Outputs are sufficient for `design_brief_agent` to proceed without client-provided brand assets.
