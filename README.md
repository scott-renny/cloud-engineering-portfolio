# Cloud Engineering Portfolio
**Scott Renny · Hands-on cloud engineering and security · AWS first**

A growing portfolio of cloud systems designed, built, secured, validated, and cleaned up with clear engineering evidence. AWS is the starting point, followed by Azure and GCP; multi-cloud work will follow demonstrated needs and completed provider foundations.

**Current status — September 26, 2026:** All five AWS onboarding credit activities are complete: Budgets, EC2, Bedrock, Lambda web app, and RDS/Aurora. **[Family IT Help Desk](aws/projects/family-it-helpdesk/README.md)** remains the retained serverless project, and v0.2 authenticated ticket management is complete after end-to-end lifecycle validation. The disposable Aurora PostgreSQL lab was validated with IAM authentication and SQL operations, then fully removed.

The [completion record](aws/COMPLETION-RECORD.md) distinguishes observed results, retained resources, and unverified billing/reward details.

## Start here
| Sequence | Project | Engineering focus | Status |
|---|---|---|---|
| 1 | [AWS Budgets](aws/fundamentals/aws-budgets/README.md) | Cost visibility and spending controls | Complete · retained |
| 2 | [EC2](aws/compute/ec2/README.md) | Secure compute lifecycle | Complete · instance/EBS removed |
| 3 | [RDS/Aurora](aws/projects/rds/README.md) | Managed PostgreSQL, IAM DB authentication, lifecycle and cleanup | Complete · cluster/backups removed |
| 4 | [Lambda](aws/serverless/lambda/README.md) | Serverless application, authenticated ticket workflow and scoped execution | Complete · Help Desk v0.2 |
| 5 | [Bedrock](aws/projects/bedrock/README.md) | Bounded foundation-model evaluation | Complete · two-request evaluation |

See the [AWS activity guide](aws/README.md) for eligibility checks and the completion workflow. Completed entries contain recorded outcomes, including the completed RDS/Aurora case study and teardown.

## Portfolio structure
```text
cloud-engineering-portfolio/
├── README.md
├── aws/
│   ├── fundamentals/
│   ├── networking/
│   ├── iam-security/
│   ├── compute/
│   ├── serverless/
│   ├── monitoring/
│   └── projects/
├── azure/
│   ├── entra-id/
│   ├── networking/
│   ├── compute/
│   ├── security/
│   └── projects/
├── gcp/
├── multi-cloud/
├── architecture/
└── templates/
```

## What a finished project demonstrates
Each case study explains an objective, architecture, implementation, security decisions, validation results, troubleshooting, cost and cleanup, and lessons learned. Use the [project template](templates/PROJECT-TEMPLATE.md) to connect each claim to a small set of sanitized evidence.

A project is complete when its agreed minimum outcome works, essential security and validation checks pass, and cleanup or explicitly accepted ongoing operation is recorded. Optional enhancements stay in a future-work list and do not reopen a completed milestone. Finish one bounded project before expanding its scope.

Statuses are **Planned**, **In progress**, **Blocked**, and **Complete**. Record blockers precisely. Never substitute a successful resource-creation screenshot for functional validation.

## Cost discipline
The target is **$0 additional out-of-pocket cost**, not unlimited use of credits. Verify the account plan, eligible credits, expiration, regional pricing, and every dependent service before provisioning. Credits are finite and may not cover every charge. If coverage or cost is uncertain, pause the deployment and complete the design locally.

Keep experiments small, short-lived, and manually controlled. Budget alerts are visibility controls, not a hard spending cap. Record estimated and observed usage separately from credit rewards. Clean up in the same session, then revisit billing after usage data has settled. The budget and Family IT Help Desk services are deliberately retained for use. Exact ongoing charges remain unverified; $0 additional cost is the operating target, not a measured billing claim.

## Connected engineering work
| Work | Relationship to this portfolio |
|---|---|
| [Cyber Operations Center (COC)](https://github.com/scott-renny/cyber-operations-center-engineering-program) | Future cloud telemetry and defensive operations integration. This repository documents cloud architecture and controls; COC owns the operational detection and response perspective. |
| [Project Ares](https://github.com/scott-renny/project_ares) | Future isolated, authorized cloud detection validation with separate lab credentials and explicit teardown. Integration is planned. |
| [Oberon integration note](architecture/oberon-integration.md) | Future AI engineering connection. The related [Oberon repository](https://github.com/scott-renny/oberon) is now available; no deployed cloud integration is claimed yet. |

## Progression
1. Preserve the completed AWS starter milestones and continue cost monitoring for intentionally retained services.
2. Extend AWS into least-privilege IAM, VPC design, logging, encryption, and repeatable infrastructure.
3. Plan and establish Azure identity, networking, compute, and security foundations; Azure planning began after completion of the AWS starter activities.
4. Add GCP foundations, then justify cross-cloud projects through concrete requirements.

Only delivered results belong in completed-project summaries. Publish concise decisions and representative evidence; keep credentials, raw account exports, private infrastructure details, and sensitive screenshots out of Git.
