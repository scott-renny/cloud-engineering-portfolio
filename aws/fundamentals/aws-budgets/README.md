# AWS Budgets — cost visibility
**Status: Complete · September 12, 2026 EDT · Budget retained**

## Objective and architecture
Establish an early-warning budget before deploying learning workloads.
AWS billing data → monthly cost budget → private email recipient.

## Implementation and security decisions
The recorded configuration used AWS-Lab-Monthly-Budget, a $10 USD monthly threshold, all AWS services, and alerts at 85% actual, 100% actual, and 100% forecasted spend. The amount is an alert threshold, not permission to incur $10 out of pocket. Recipient details remain private.

## Validation
The onboarding activity subsequently showed Completed with a $20 award. Alert settings were reviewed before creation; delivery of a threshold-triggered budget email was not demonstrated. No artificial spend was generated to test an alert.

## Troubleshooting
The reward initially remained Not started after creation. The workflow continued without creating duplicate budgets; a later console checkpoint showed completion.

## Cost and cleanup
Retained intentionally for ongoing AWS cost visibility. A budget is not a hard spending cap. Actual usage, credit coverage and retained feature costs require periodic billing review; no measured $0 bill is claimed.

## Lessons learned
Set cost visibility before provisioning, and separate reward-processing delays from resource failure. See the [completion record](../../COMPLETION-RECORD.md).
