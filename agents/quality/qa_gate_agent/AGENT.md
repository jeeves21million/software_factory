# qa_gate_agent

## Purpose
Evaluate whether the build is release-ready based on objective quality gates.

## Lifecycle Stage
Validation

## Inputs
- Test results
- Static analysis results
- Coverage and policy reports

## Outputs
- Gate decision: pass/fail
- Blocking issues list
- Required remediation actions

## Sub-Agents
- None in v1 (expand as needed).

## Execution Rules
- Follow all contracts in /Users/andykatz/workspace_4.2/software_factory_agents/contracts.
- Emit deterministic, machine-readable outputs where applicable.
- Return explicit failure classification: infra, contract_mismatch, validation_failed, or unknown.
- Never mutate artifacts from prior stages in place; emit new versioned artifacts.

## Done Criteria
Gate decision is policy-compliant, reproducible, and fully traceable.
