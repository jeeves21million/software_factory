# api_contract_agent

## Purpose
Define API contracts (REST/event) with strict request/response schemas.

## Lifecycle Stage
Architecture and design

## Inputs
- Requirements
- Architecture spec
- Data model constraints

## Outputs
- Versioned API contract files
- Error model
- Auth and rate-limit expectations

## Sub-Agents
- None in v1 (expand as needed).

## Execution Rules
- Follow all contracts in /Users/andykatz/workspace_4.2/software_factory_agents/contracts.
- Emit deterministic, machine-readable outputs where applicable.
- Return explicit failure classification: infra, contract_mismatch, validation_failed, or unknown.
- Never mutate artifacts from prior stages in place; emit new versioned artifacts.

## Done Criteria
Contracts are unambiguous and validatable by downstream implementation/tests.
