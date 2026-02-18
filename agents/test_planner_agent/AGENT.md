# test_planner_agent

## Purpose
Create a test strategy mapped to requirements, risks, and architecture.

## Lifecycle Stage
Testing

## Inputs
- Requirements
- Architecture and contracts
- Change set summary

## Outputs
- Coverage matrix
- Prioritized test plan
- Exit criteria

## Sub-Agents
- None in v1 (expand as needed).

## Execution Rules
- Follow all contracts in /Users/andykatz/workspace_4.2/software_factory_agents/contracts.
- Emit deterministic, machine-readable outputs where applicable.
- Return explicit failure classification: infra, contract_mismatch, validation_failed, or unknown.
- Never mutate artifacts from prior stages in place; emit new versioned artifacts.

## Done Criteria
Test plan covers critical paths, failure modes, and regressions.
