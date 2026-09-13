# Amazon Bedrock — starter case study
**Status: Planned · Execution: Not started · Reward: Not checked · Cost closure: Not started**

## Objective
Run a bounded foundation-model playground evaluation and record output quality and inference cost.

## Proposed architecture
Operator with scoped access → Bedrock playground → selected foundation model. Final configuration and diagram will be recorded after account eligibility and cost checks.

## Planned implementation
Follow the eligible playground activity. Record model ID, region, prompt, output limit, and a small fixed number of requests; use synthetic prompts.

## Security decisions to validate
Do not submit personal data or secrets. Avoid provisioned capacity and unrelated agents or knowledge bases; verify model access and pricing before invoking.

## Acceptance and evidence
Record a sanitized prompt/response, model/settings, one defined quality criterion, and observed usage. Treat generated text as untrusted output.
Actual results: **Not run**. Add sanitized evidence; no completion claim is supported yet.

## Troubleshooting
Pending execution. Record observed symptoms, cause, fix, and retest; do not invent failures.

## Cost and cleanup
Target: **$0 additional out-of-pocket cost**. Confirm eligible credits and current regional service/dependency pricing before creating resources. Record estimate, runtime, observed charges, credits applied, and later billing review separately.

End testing and inspect any explicitly created resources or logging. Record whether only on-demand inference was used; verify no provisioned throughput or other persistent dependencies remain.

## Lessons learned
Pending execution.

## Completion
Complete the minimum outcome, security checks, cleanup verification, and cost record before marking complete. Track promotional reward status separately. Optional extensions do not block completion.

Follow the [AWS activity guide](../../README.md) and expand this brief using the [project template](../../../templates/PROJECT-TEMPLATE.md).
