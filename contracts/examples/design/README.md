# Design Contract Examples

Use a two-layer model:

1. `human_inputs/`
- What humans actually provide (notes, markdown, text manifests, links to PDFs/docs/images).

2. `normalized/`
- Structured JSON produced by a normalizer step for machine-to-machine agent contracts.

## Layout
- `human_inputs/startup_with_brand_assets/`
- `human_inputs/startup_without_brand_assets/`
- `normalized/design_intake_normalizer_agent/`
- `normalized/design_brief_agent/`

## Important
Humans should not be asked to author contract JSON directly. JSON is internal pipeline format.

## Legacy
Existing per-agent JSON examples in sibling folders are internal references for agent contract validation.
