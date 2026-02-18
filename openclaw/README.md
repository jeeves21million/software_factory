# OpenClaw Integration Spec

This folder defines how app repos invoke the software factory design pipeline in OpenClaw.

## Files
- `design_run.schema.json`: Schema for `.openclaw/design_run.yaml` in app repos.
- `design_run.example.yaml`: Example manifest for a PRD + use-case-flow driven design run.
- `worker_entrypoint_contract.md`: Minimum worker behavior and response contract.

## App Repo Convention
Add a manifest at `.openclaw/design_run.yaml` in the app repo and point OpenClaw to it.

## Accessibility Fallback Rule
If no explicit accessibility constraints file is provided, worker must default to `wcag_2_2_aa`, emit a warning in trace, and continue the run.
