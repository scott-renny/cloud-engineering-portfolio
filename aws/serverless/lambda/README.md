# AWS Lambda — starter case study
**Status: Planned · Execution: Not started · Reward: Not checked · Cost closure: Not started**

## Objective
Build a small web application and verify its response and access control.

## Proposed architecture
Test client → function URL → Lambda execution role → response/logs. Final configuration and diagram will be recorded after account eligibility and cost checks.

## Planned implementation
Follow the eligible web-app activity using a function URL. Record runtime, handler, memory, timeout, URL authentication, and minimal test payload.

## Security decisions to validate
Use a narrowly scoped execution role, synthetic data, and bounded execution. Record and justify any temporary public access required by the activity.

## Acceptance and evidence
Verify the expected HTTP response and inspect errors/logs. Test the chosen authentication boundary; record any intentional public exposure.
Actual results: **Not run**. Add sanitized evidence; no completion claim is supported yet.

## Troubleshooting
Pending execution. Record observed symptoms, cause, fix, and retest; do not invent failures.

## Cost and cleanup
Target: **$0 additional out-of-pocket cost**. Confirm eligible credits and current regional service/dependency pricing before creating resources. Record estimate, runtime, observed charges, credits applied, and later billing review separately.

Remove the function URL and function, unused versions/layers, project-specific roles/policies, and unneeded log groups. Check for related resources created by the activity.

## Lessons learned
Pending execution.

## Completion
Complete the minimum outcome, security checks, cleanup verification, and cost record before marking complete. Track promotional reward status separately. Optional extensions do not block completion.

Follow the [AWS activity guide](../../README.md) and expand this brief using the [project template](../../../templates/PROJECT-TEMPLATE.md).
