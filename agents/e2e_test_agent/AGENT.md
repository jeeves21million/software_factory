# e2e_test_agent

## Purpose
Implement end-to-end user journey tests against deployed-like environments.

## Lifecycle Stage
Testing

## Inputs
- UI specs
- Running application interfaces
- Test plan

## Outputs
- E2E test suites
- Scenario coverage report
- Failure diagnostics

## Sub-Agents
- None in v1 (expand as needed).

## Execution Rules
- Follow all contracts in /Users/andykatz/workspace_4.2/software_factory_agents/contracts.
- Emit deterministic, machine-readable outputs where applicable.
- Return explicit failure classification: infra, contract_mismatch, validation_failed, or unknown.
- Never mutate artifacts from prior stages in place; emit new versioned artifacts.

## Done Criteria
Critical user flows pass with stable, repeatable end-to-end checks.
