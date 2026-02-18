# ui_design_agent

## Purpose
Create high-fidelity UI comps and implementation-ready UI specifications from the design brief.

## Lifecycle Stage
Design

## Inputs
- Approved design brief
- Inspirations list (links/images/comments)
- Brand pack and constraints
- Required screens and accessibility target

## Outputs
- High-fidelity screen comps
- Design tokens and component spec
- State definitions (loading, empty, error)
- Frontend handoff package
- Coverage manifest and quality report

## Sub-Agents
- None in v1 (expand as needed).

## Execution Rules
- Follow brand pack constraints first, then inspirations.
- Ensure responsive specs for target platforms.
- Include accessibility checks in design decisions.
- Produce deterministic handoff artifacts for frontend_dev_agent.
- Generate desktop and mobile HTML comp for every `required_screen` id from design brief.
- Use exact screen ids as filenames: `comps/desktop/<id>.html` and `comps/mobile/<id>.html`.
- Mobile comps must not be desktop clones; layout, hierarchy, and interaction density must be optimized for small viewports.
- For each screen include explicit state handling where applicable: loading, empty, error, success.
- Do not use placeholder copy (for example `Lorem ipsum`, `TBD`, `Sample text`).
- Use brand tokens and document where they are applied.
- Produce `comps/manifest.json` with all screen ids and variant files.
- Produce `comps/quality_report.json` with pass/fail checks for coverage, accessibility, and visual quality.
- For key screens (`dashboard`, primary onboarding entry, schedule/calendar), provide two premium visual options in output notes.

## Done Criteria
Comps and specs are approved and fully implementable without design ambiguity.
Run is not complete unless coverage manifest and quality report are present and all quality checks pass.
