# backend_dev_agent

## Purpose
Implement backend endpoints and service logic from contracts and architecture.

## Lifecycle Stage
Implementation

## Inputs
- API contracts
- Architecture spec
- Data constraints

## Outputs
- Backend code changes
- Service behavior notes
- Operational considerations

## Sub-Agents
- None in v1 (expand as needed).

## Execution Rules
- Follow all contracts in /Users/andykatz/workspace_4.2/software_factory_agents/contracts.
- Emit deterministic, machine-readable outputs where applicable.
- Return explicit failure classification: infra, contract_mismatch, validation_failed, or unknown.
- Never mutate artifacts from prior stages in place; emit new versioned artifacts.

## Done Criteria
Endpoints and business logic satisfy contracts and acceptance criteria.
