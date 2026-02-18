# Software Factory Agents

This repository contains reusable agent definitions and supporting assets for a software factory that can build production-ready software from ideas.

## Directory Layout

### `agents/`
- Agent and sub-agent definitions.
- Each agent folder should include: role/purpose, inputs, outputs, prompt/instructions, tools allowed, guardrails, and retry/failure behavior.

### `contracts/`
- Machine-readable schemas (usually JSON Schema) for all agent I/O.
- Versioned contracts so the orchestrator can validate payloads before and after each stage.

### `workflows/`
- Pipeline stage definitions and transition rules.
- Defines legal flow paths (for example, design -> implementation -> test -> fix loop) and gate criteria per stage.

### `policies/`
- Global standards: security, code quality, testing thresholds, dependency rules, and compliance checks.
- Agents read and apply these rules during generation and review.

### `evals/`
- Evaluation tasks and expected outcomes for agent quality.
- Includes regression suites to detect prompt/behavior drift before releasing new agent versions.

### `templates/`
- Reusable project scaffolds and snippets (API service skeletons, frontend component patterns, CI configs, migration templates).
- Agents should prefer these for consistency and speed.

### `versions/`
- Compatibility and release metadata.
- `compatibility.yaml` maps `agent-pack version` to supported `orchestrator/core versions` and contract versions.
