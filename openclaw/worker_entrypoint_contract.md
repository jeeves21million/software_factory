# OpenClaw Worker Entrypoint Contract

## Objective
Define the minimum request/response contract for a worker that executes a design run from an app repo manifest.

## Entrypoint
`design-run`

## Required CLI Arguments
- `--app-repo-url`: Git URL of target app repo.
- `--app-repo-ref`: Git ref to run against (branch, tag, or commit).
- `--manifest-path`: Path to design run manifest inside app repo (for example `.openclaw/design_run.yaml`).
- `--workspace-root`: Local execution root for cloned repos and artifacts.

## Required Behavior
1. Clone app repo at `--app-repo-ref`.
2. Read and validate manifest using `openclaw/design_run.schema.json` from pinned agent pack.
3. Clone agent pack repo at `agent_pack_ref` from manifest.
4. Build normalized input payload from human input files listed in manifest.
5. Apply runtime defaults before agent execution:
   - If no explicit accessibility constraints are provided (for example no `inputs.extra_context` accessibility file), set `accessibility_target` to `wcag_2_2_aa`.
   - Emit a warning event in trace/logs for this defaulting action.
   - Do not fail the run solely because optional accessibility input files are absent.
6. Execute design flow with routing rules:
   - Research optional.
   - Brand foundation optional and used only when brand assets are missing or forced.
7. Validate each agent I/O payload against schemas in `contracts/agents/`.
8. Write artifacts and trace files to app repo paths defined in manifest outputs.
9. Commit outputs to a new branch (`pr_branch_prefix/run_id`) and open PR when `open_pr=true`.

## Stage Pipeline (default)
- `design_intake_normalizer_agent`
- `ui_research_agent` (optional)
- `brand_foundation_agent` (optional)
- `design_brief_agent`
- `ui_design_agent`
- `ui_ux_spec_agent` (optional)

## Minimum Response (stdout JSON)
```json
{
  "run_id": "pulsebudget-design-001",
  "status": "success",
  "executed_stages": [
    "design_intake_normalizer",
    "design_brief",
    "ui_design"
  ],
  "artifact_dir": "artifacts/design/pulsebudget-design-001",
  "trace_file": "artifacts/design/pulsebudget-design-001/trace/events.jsonl",
  "branch": "openclaw/design/pulsebudget-design-001",
  "pr_url": "https://github.com/your-org/your-app-repo/pull/123"
}
```

## Failure Response (stdout JSON)
```json
{
  "run_id": "pulsebudget-design-001",
  "status": "failed",
  "failed_stage": "design_intake_normalizer",
  "error_category": "validation_failed",
  "message": "Missing required file: docs/flows/calendar_scheduling.md",
  "retryable": false
}
```
