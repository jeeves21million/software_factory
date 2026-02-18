# ui_ux_spec_agent

## Purpose
Define user flows, screen states, interaction contracts, and design tokens.

## Lifecycle Stage
Architecture and design

## Inputs
- Requirements
- Architecture constraints
- Brand/product guidance

## Outputs
- UI/UX specification
- Component/state definitions
- Design token set

## Sub-Agents
- None in v1 (expand as needed).

## Execution Rules
- Follow all contracts in /Users/andykatz/workspace_4.2/software_factory_agents/contracts.
- Emit deterministic, machine-readable outputs where applicable.
- Return explicit failure classification: infra, contract_mismatch, validation_failed, or unknown.
- Never mutate artifacts from prior stages in place; emit new versioned artifacts.

## Done Criteria
Specs are complete enough for implementation and e2e validation.
