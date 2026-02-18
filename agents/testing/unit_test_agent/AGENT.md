# unit_test_agent

## Purpose
Implement unit tests for isolated logic and edge cases.

## Lifecycle Stage
Testing

## Inputs
- Code changes
- Test plan
- Coding/testing standards

## Outputs
- Unit test files
- Coverage notes
- Failure diagnostics

## Sub-Agents
- None in v1 (expand as needed).

## Execution Rules
- Follow all contracts in /Users/andykatz/workspace_4.2/software_factory_agents/contracts.
- Emit deterministic, machine-readable outputs where applicable.
- Return explicit failure classification: infra, contract_mismatch, validation_failed, or unknown.
- Never mutate artifacts from prior stages in place; emit new versioned artifacts.

## Done Criteria
Core logic and edge conditions are validated with deterministic unit tests.
