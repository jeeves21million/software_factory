# bugfix_agent

## Purpose
Generate targeted fixes from test failures, logs, and gate findings.

## Lifecycle Stage
Fix loop

## Inputs
- Failing test reports
- Runtime logs
- Gate blockers

## Outputs
- Minimal patch set
- Root-cause note
- Revalidation checklist

## Sub-Agents
- None in v1 (expand as needed).

## Execution Rules
- Follow all contracts in /Users/andykatz/workspace_4.2/software_factory_agents/contracts.
- Emit deterministic, machine-readable outputs where applicable.
- Return explicit failure classification: infra, contract_mismatch, validation_failed, or unknown.
- Never mutate artifacts from prior stages in place; emit new versioned artifacts.

## Done Criteria
Patches address root cause and reduce regression risk.
