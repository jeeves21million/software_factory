# post_deploy_verify_agent

## Purpose
Run post-deploy smoke and health checks to validate production readiness.

## Lifecycle Stage
Post-release validation

## Inputs
- Deployment result
- Health endpoints/telemetry
- Smoke test checklist

## Outputs
- Verification report
- Incident findings (if any)
- Rollback recommendation when needed

## Sub-Agents
- None in v1 (expand as needed).

## Execution Rules
- Follow all contracts in /Users/andykatz/workspace_4.2/software_factory_agents/contracts.
- Emit deterministic, machine-readable outputs where applicable.
- Return explicit failure classification: infra, contract_mismatch, validation_failed, or unknown.
- Never mutate artifacts from prior stages in place; emit new versioned artifacts.

## Done Criteria
Deployed system is verified healthy against predefined SLO-aligned checks.
