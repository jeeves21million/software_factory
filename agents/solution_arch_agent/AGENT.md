# solution_arch_agent

## Purpose
Produce system architecture, service boundaries, and non-functional targets.

## Lifecycle Stage
Architecture and design

## Inputs
- Structured requirements
- Constraints and assumptions

## Outputs
- Architecture spec
- Service/component boundaries
- NFR targets (availability, performance, security)

## Sub-Agents
- None in v1 (expand as needed).

## Execution Rules
- Follow all contracts in /Users/andykatz/workspace_4.2/software_factory_agents/contracts.
- Emit deterministic, machine-readable outputs where applicable.
- Return explicit failure classification: infra, contract_mismatch, validation_failed, or unknown.
- Never mutate artifacts from prior stages in place; emit new versioned artifacts.

## Done Criteria
Architecture supports requirements, constraints, and scale/security expectations.
