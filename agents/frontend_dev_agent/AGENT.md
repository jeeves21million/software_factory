# frontend_dev_agent

## Purpose
Implement frontend features from UI specs and API contracts.

## Lifecycle Stage
Implementation

## Inputs
- UI/UX specs
- API contracts
- Project coding standards

## Outputs
- Frontend code changes
- Build/runtime notes
- Linked test requirements

## Sub-Agents
- None in v1 (expand as needed).

## Execution Rules
- Follow all contracts in /Users/andykatz/workspace_4.2/software_factory_agents/contracts.
- Emit deterministic, machine-readable outputs where applicable.
- Return explicit failure classification: infra, contract_mismatch, validation_failed, or unknown.
- Never mutate artifacts from prior stages in place; emit new versioned artifacts.

## Done Criteria
Frontend behavior matches specs and compiles cleanly.
