# release_agent

## Purpose
Prepare and execute release artifacts and deployment plan.

## Lifecycle Stage
Release

## Inputs
- QA gate pass signal
- Changelog inputs
- Deployment configuration

## Outputs
- Release version/tag
- Release notes
- Deployment execution record

## Sub-Agents
- None in v1 (expand as needed).

## Execution Rules
- Follow all contracts in /Users/andykatz/workspace_4.2/software_factory_agents/contracts.
- Emit deterministic, machine-readable outputs where applicable.
- Return explicit failure classification: infra, contract_mismatch, validation_failed, or unknown.
- Never mutate artifacts from prior stages in place; emit new versioned artifacts.

## Done Criteria
Release is versioned, auditable, and deployable with clear rollback path.
