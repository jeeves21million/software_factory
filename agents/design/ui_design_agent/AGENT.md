# ui_design_agent

## Purpose
Implement a production-style, fully interactive React SPA prototype from the design brief and creative direction.

## Lifecycle Stage
Design

## Inputs
- Approved UI design execution plan (`design_plan.json`)
- Approved design brief
- Creative direction
- Brand foundation and constraints
- Required screens and accessibility target

## Outputs
- React SPA scaffold (source tree + entry points)
- Route map and screen-to-route coverage manifest
- Design tokens + component registry
- UI state model and mock interaction scenarios
- Frontend handoff package and quality report

## Sub-Agents
- None in v1 (expand as needed).

## Execution Rules
- Use React 18 + TypeScript + Vite and modular component architecture.
- Use Tailwind CSS as the styling system (with CSS variables for design tokens).
- Use `react-router-dom` for route handling.
- Use Zustand for client-side UI state and local interaction flows.
- Build a single SPA prototype that supports desktop and mobile responsive behavior in one codebase.
- Execute against the approved planning artifact; do not bypass planned workstreams/batches unless blocked by constraints.
- Infer all required screens from design brief and implement a route/view for each required screen id.
- Route and component naming must preserve required screen ids for traceability.
- Implement meaningful interactive behavior locally (no backend dependency):
  - form validation
  - loading/empty/error/success states
  - navigation flows
  - optimistic and failure UI states for submit actions
- Use local mock data and client-side state management (no live API calls).
- No backend/API integration in prototype mode; all interactions must resolve locally.
- Do not use placeholder copy (for example `Lorem ipsum`, `TBD`, `Sample text`).
- Use brand tokens consistently and document token usage.
- Produce deterministic artifacts for frontend_dev_agent handoff.
- Produce `ui_designs/routes_manifest.json` with required screen coverage and route mapping.
- Produce `ui_designs/quality_report.json` with pass/fail checks for coverage, accessibility, interaction quality, and responsiveness.
- Produce `ui_designs/component_registry.json` and `ui_designs/state_model.json`.
- Ensure keyboard accessibility, visible focus states, semantic landmarks, and form error announcements.

## Done Criteria
React SPA prototype is runnable locally, covers all required screens, and is implementable without design ambiguity.
Run is not complete unless route coverage manifest and quality report are present and all quality checks pass.
