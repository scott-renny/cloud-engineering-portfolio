# Amazon RDS — starter case study
**Status: Planned · Execution: Not started · Reward: Not checked · Cost closure: Not started**

## Objective
Create a minimal managed database and explain isolation, configuration, and lifecycle choices.

## Proposed architecture
Authorized client, if needed → restricted database endpoint → managed storage. Final configuration and diagram will be recorded after account eligibility and cost checks.

## Planned implementation
Follow the eligible activity; record engine, size, storage, availability choice, backup retention, region, and runtime. Add a small synthetic query only if access can be arranged within scope and cost limits.

## Security decisions to validate
Keep the database private where supported by the activity; restrict database access and keep credentials out of Git.

## Acceptance and evidence
Verify available state and configuration. If claiming database connectivity, include a successful synthetic query and an access-boundary check; otherwise label connectivity as untested.
Actual results: **Not run**. Add sanitized evidence; no completion claim is supported yet.

## Troubleshooting
Pending execution. Record observed symptoms, cause, fix, and retest; do not invent failures.

## Cost and cleanup
Target: **$0 additional out-of-pocket cost**. Confirm eligible credits and current regional service/dependency pricing before creating resources. Record estimate, runtime, observed charges, credits applied, and later billing review separately.

Delete the disposable database and inspect retained snapshots, automated backups, monitoring, secrets, and dependent resources. Skip a final snapshot only for explicitly disposable synthetic data.

## Lessons learned
Pending execution.

## Completion
Complete the minimum outcome, security checks, cleanup verification, and cost record before marking complete. Track promotional reward status separately. Optional extensions do not block completion.

Follow the [AWS activity guide](../../README.md) and expand this brief using the [project template](../../../templates/PROJECT-TEMPLATE.md).
