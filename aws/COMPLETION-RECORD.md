# AWS completion record
**Reconciled September 14, 2026**

This record summarizes the owner's September 12–13 EDT lab work in *Cloud Account Timing*, including console screenshots, command results, deployment confirmations, and explicit acceptance. The Help Desk acceptance occurred September 13 EDT / September 14 UTC. This documentation pass reviewed the supplied final ticket and DynamoDB screenshots; it did not repeat live AWS tests or inspect current billing.

## Milestone register
| Work | Engineering status | Resource disposition | Reward evidence |
|---|---|---|---|
| [Account baseline](iam-security/account-baseline/README.md) | Initial controls established | Account retained | Initial $100 credit recorded |
| [Budgets](fundamentals/aws-budgets/README.md) | Complete | Budget retained intentionally | $20 completion recorded |
| [EC2](compute/ec2/README.md) | Complete | Instance terminated; root EBS deletion verified | $20 completion recorded |
| [Bedrock](projects/bedrock/README.md) | Complete | Two on-demand requests ended; no persistent Bedrock resources created | $20 completion recorded |
| [Lambda / Help Desk v0.1](projects/family-it-helpdesk/README.md) | Complete | App and supporting services retained intentionally | Later Lambda reward confirmation not present in reviewed record |
| [RDS](projects/rds/README.md) | Planned | No deployment evidenced | No award evidenced |

The latest reviewed activity summary showed **3/5 and $60 additional credits earned**, after Bedrock. That is a historical checkpoint, not today's balance. Neither a fourth reward nor all $200 is claimed. DynamoDB persistence does not satisfy or substitute for the separate RDS activity.

## Evidence and limits
- EC2 acceptance: successful SSH, Linux and network inspection, metadata denial without a token and successful IMDSv2 use, package installation, encrypted EBS inspection, termination and missing-volume confirmation.
- Bedrock: initial and revised model responses reviewed; total counters reported as 392 input / 418 output tokens.
- Help Desk: final UI receipt and DynamoDB scan show the same test ticket; owner explicitly confirmed email receipt. The UI shows Medium priority and Submitted status, and the scan returns two records.
- Earlier security-category test produced Critical priority. The final record demonstrates the approved-user path; independent post-hardening negative tests for unapproved API calls/direct Function URL POST are not reproduced in this documentation pass.
- Screenshots contain private account/contact information elsewhere in the session. Raw captures, credentials, live endpoints, and ticket contents are not copied into this public repository.
- Published source code is not a deployment export. This update publishes case studies and recorded behavior, not a claim that an infrastructure-as-code build exists.

## Cost closure
The operating target remains $0 additional out-of-pocket cost. Historical credit awards are distinct from usage charges. Exact EC2, inference, and ongoing Help Desk billing totals were not supplied. Retained resources are intentional; billing review remains an operational follow-up and does not reopen accepted functional milestones.

## Next bounded work
v0.2: admin identity boundary, ticket list/detail/status APIs, then the management UI and real status progression. The user authorized starting this version; the last checkpoint requested creation of HelpDeskAdmins, with no confirmation yet.

v0.3: optional bounded Bedrock troubleshooting, only after v0.2; the conventional help desk remains independent of AI. RDS remains a separate starter activity. COC/Ares integrations remain future work.
