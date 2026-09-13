# Amazon EC2 — starter case study
**Status: Planned · Execution: Not started · Reward: Not checked · Cost closure: Not started**

## Objective
Launch, inspect, and terminate a minimal instance while demonstrating a restricted network boundary.

## Proposed architecture
Operator → scoped management access → EC2 instance + volume in a VPC. Final configuration and diagram will be recorded after account eligibility and cost checks.

## Planned implementation
Follow the eligible activity; record AMI, size, disk, region, security group, and runtime. Use the minimum required functional check.

## Security decisions to validate
Avoid unrestricted management ingress; use scoped access and no embedded credentials. Document disk encryption and any public-IP choice.

## Acceptance and evidence
Verify running/health state, the intended basic workload or management check, and effective inbound rules. Record evidence before termination.
Actual results: **Not run**. Add sanitized evidence; no completion claim is supported yet.

## Troubleshooting
Pending execution. Record observed symptoms, cause, fix, and retest; do not invent failures.

## Cost and cleanup
Target: **$0 additional out-of-pocket cost**. Confirm eligible credits and current regional service/dependency pricing before creating resources. Record estimate, runtime, observed charges, credits applied, and later billing review separately.

Terminate the instance; inspect leftover EBS volumes, snapshots, public/Elastic IPs, and any created networking or logs. Stopping alone is not cleanup.

## Lessons learned
Pending execution.

## Completion
Complete the minimum outcome, security checks, cleanup verification, and cost record before marking complete. Track promotional reward status separately. Optional extensions do not block completion.

Follow the [AWS activity guide](../../README.md) and expand this brief using the [project template](../../../templates/PROJECT-TEMPLATE.md).
