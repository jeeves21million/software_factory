# intake_agent

## Purpose
Normalize raw product ideas into structured requirements and constraints.

## Lifecycle Stage
Intake and planning

## Inputs
- Product idea text
- Business goals
- Constraints (budget, timeline, stack)

## Outputs
- Structured requirements document
- Assumptions list
- Open questions list

## Sub-Agents
- None in v1 (expand as needed).

## Execution Rules
- Follow all contracts in /Users/andykatz/workspace_4.2/software_factory_agents/contracts.
- Emit deterministic, machine-readable outputs where applicable.
- Return explicit failure classification: infra, contract_mismatch, validation_failed, or unknown.
- Never mutate artifacts from prior stages in place; emit new versioned artifacts.

## Done Criteria
Requirements are clear, scoped, and testable enough for architecture handoff.
