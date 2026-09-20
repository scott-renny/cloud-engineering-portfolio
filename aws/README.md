# AWS
**Status — September 20, 2026:** All five AWS onboarding credit activities are complete: Budgets, EC2, Bedrock, Lambda web app, and RDS/Aurora. The Family IT Help Desk remains the retained serverless application; disposable EC2 and Aurora lab resources were removed. See the [completion record](COMPLETION-RECORD.md) for evidence, retention, reward, and cleanup status.

Start with [Budgets](fundamentals/aws-budgets/README.md), then [EC2](compute/ec2/README.md), [RDS/Aurora](projects/rds/README.md), [Lambda](serverless/lambda/README.md), and [Bedrock](projects/bedrock/README.md).

## Credit activity entry point
AWS lists five onboarding activities for additional credits. The account completed all five by September 20, 2026. The final RDS/Aurora activity was validated with a live IAM-authenticated PostgreSQL session before teardown.

Before future credit-backed work, privately record account eligibility, displayed completion deadline, available credits and expiry, region, selected configuration, estimated usage, and cleanup plan. Never publish the account ID, live credentials, authentication tokens, or billing exports.

Source originally checked September 12, 2026: [AWS — Earning additional credits](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/free-tier-plans-activities.html). [Free Tier FAQs](https://aws.amazon.com/free/free-tier-faqs/) explain account-specific credit and expiration checks. Recheck current terms before new deployments.

## Completion workflow
1. Choose one bounded lab and define minimum acceptance checks.
2. Verify cost coverage for the service and dependencies.
3. Use the smallest suitable configuration.
4. Capture sanitized functional and security evidence.
5. Remove temporary resources and verify dependent-resource cleanup.
6. Check activity/reward status separately from technical completion.
7. Review delayed billing data and keep point-in-time balances distinct from future cost claims.

Keep engineering status, reward status, and cost-closure status distinct. A functioning lab can have a pending reward; unresolved resource cleanup remains a completion blocker. Optional enhancements do not reopen accepted milestones.

Use the [template](../templates/PROJECT-TEMPLATE.md) for future case studies.
