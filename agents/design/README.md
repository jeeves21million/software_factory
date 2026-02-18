# Design Agents

This group handles design research, brief creation, and UI design outputs.

## Design Phase Dependencies

The design phase can start when these inputs are available:
- Product context: product idea/summary, target users, and platform target (`web` or `native_mobile`).
- Business context: goals, constraints, and success criteria from intake.
- Brand context: brand guidelines and logos (required), plus colors/fonts if available.
- Inspirations: one or more entries using the shared format (`type`, `value`, `comment`).
- Scope context: required screens, key user flows, and any accessibility/legal constraints.

Required upstream artifacts:
- Intake requirements artifact from `intake_agent`.
- If research path is used, research pack from `ui_research_agent`.

## Agent Dependencies

### `ui_research_agent` (optional)
Purpose: Optional startup UX/UI pattern research and inspiration assembly.

Required inputs:
- `product_idea`
- `target_audience`
- `platform`

Optional inputs:
- `seed_inspirations`

Produces:
- Similar product references
- Common flow patterns
- Structured `inspirations` candidates

Primary downstream dependency:
- Feeds `design_brief_agent`.

### `design_brief_agent`
Purpose: Produces a structured design brief from client or research inputs.

Required inputs:
- `project_summary`
- `inspirations`
- `brand_pack` (must include `brand_guidelines` and `logos`)

Optional inputs:
- `existing_design_files` (Figma/other design sources)
- `content_assets`, `copy_assets`
- `required_screens`, `product_surface`
- `accessibility_target`, `technical_constraints`
- `competitor_refs`, `must_reuse_components`, `legal_restrictions`

Produces:
- Structured design brief
- Consolidated inspirations with rationale
- Handoff payload for UI design

Primary downstream dependency:
- Feeds `ui_design_agent`.

### `ui_design_agent`
Purpose: Produces high-fidelity designs and implementation-ready UI specs.

Required inputs:
- Approved `design_brief`
- `inspirations`
- `brand_pack`
- `required_screens`

Optional inputs:
- `accessibility_target`

Produces:
- High-fidelity comp set
- Token set
- Component specs
- Screen specs/states

Primary downstream dependency:
- Feeds implementation (typically `frontend_dev_agent`).

### `ui_ux_spec_agent`
Purpose: General UI/UX specification support (legacy/general path).

Required inputs:
- Requirements from intake and architecture constraints
- UI decisions from brief/design process

Optional inputs:
- Existing product/design system context

Produces:
- UI/UX specification artifacts for implementation and e2e validation

Primary downstream dependency:
- Feeds implementation and testing stages.

## Supported Paths

- With research: `intake -> design_research -> design_brief -> design`
- Without research: `intake -> design_brief -> design`

If complete manual design-brief inputs are already provided, skip `ui_research_agent` and route directly to `design_brief_agent`.
