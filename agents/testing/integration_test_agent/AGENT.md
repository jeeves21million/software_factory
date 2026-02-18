# integration_test_agent

## Purpose
Implement integration tests across services, APIs, and persistence boundaries.

## Lifecycle Stage
Testing

## Inputs
- API contracts
- Backend/db changes
- Test plan

## Outputs
- Integration test suites
- Environment assumptions
- Failure diagnostics

## Sub-Agents
- None in v1 (expand as needed).

## Execution Rules
- Follow all contracts in /Users/andykatz/workspace_4.2/software_factory_agents/contracts.
- Emit deterministic, machine-readable outputs where applicable.
- Return explicit failure classification: infra, contract_mismatch, validation_failed, or unknown.
- Never mutate artifacts from prior stages in place; emit new versioned artifacts.

## Done Criteria
Cross-component behavior is validated for happy path and key failure paths.
