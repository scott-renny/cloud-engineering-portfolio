# AWS completion record
**Reconciled September 26, 2026**

This record summarizes completed AWS starter work and distinguishes engineering validation, retained resources, promotional activity confirmation, and cleanup. Public documentation intentionally omits account IDs, credentials, live endpoints, authentication tokens, private ticket data, and raw billing exports.

## Milestone register
| Work | Engineering status | Resource disposition | Reward evidence |
|---|---|---|---|
| [Account baseline](iam-security/account-baseline/README.md) | Initial controls established | Account retained | Initial $100 credit recorded |
| [Budgets](fundamentals/aws-budgets/README.md) | Complete | Budget retained intentionally | $20 activity completion recorded |
| [EC2](compute/ec2/README.md) | Complete | Instance terminated; root EBS deletion verified | $20 activity completion recorded |
| [Bedrock](projects/bedrock/README.md) | Complete | Two on-demand requests ended; no persistent Bedrock resources created | $20 activity completion recorded |
| [Lambda / Family IT Help Desk](projects/family-it-helpdesk/README.md) | v0.2 complete | App and supporting services retained intentionally | Lambda web-app activity completed |
| [RDS / Aurora PostgreSQL](projects/rds/README.md) | Complete | Writer and cluster deleted; no final snapshot or retained automated backup | Final $20 activity completed |

All **5/5 AWS onboarding activities** are now complete. After the final RDS/Aurora activity, the AWS Console showed **$199.97 USD credits remaining**. That is a point-in-time balance after small lab usage, not a guarantee of future cost or a claim that metered services are free.

## RDS/Aurora completion evidence
On September 20, 2026, an Aurora PostgreSQL Serverless cluster was created in `us-east-2` using Express configuration. The writer reached Available. AWS CloudShell connected with IAM database authentication over TLS 1.3; the server reported PostgreSQL 17.9.

Validation included querying the current database/user/version, creating a `cloud_lab` table, inserting one synthetic record, selecting it successfully, and cleanly exiting the PostgreSQL session.

Cleanup was explicit: the writer instance was deleted, then the cluster was deleted with final snapshot creation and automated-backup retention disabled. Post-delete checks showed Databases 0, Manual snapshots 0, and Current Region automated backups 0.

## Other evidence and limits
- EC2 acceptance included SSH, Linux/network inspection, IMDSv2 validation, package installation, encrypted EBS inspection, termination, and missing-volume confirmation.
- Bedrock included an initial and revised model evaluation with human review of recommendations.
- Family IT Help Desk v0.2 is complete: authenticated administration, backend status updates, restored authoritative state, server-side validation, security escalation behavior, and the full Submitted → In Progress → Resolved lifecycle were validated. Its retained services are intentional.
- Published source/documentation is not an infrastructure-as-code deployment export.
- Raw screenshots containing private account/contact information are not copied into this public repository.

## Cost closure
The operating target remains $0 additional out-of-pocket cost. Promotional credits and usage charges are tracked separately. Disposable EC2 and Aurora resources were removed after validation. Retained Help Desk services and the budget are intentional and should continue to be monitored.

## Next bounded work
Preserve Family IT Help Desk v0.2 as the completed baseline and proceed with the next deliberately scoped AWS engineering/security exercise. v0.3 remains the optional bounded Bedrock troubleshooting phase; the conventional help desk remains independent of AI.
