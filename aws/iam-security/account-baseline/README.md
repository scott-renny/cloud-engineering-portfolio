# AWS account baseline
**Status: Initial controls established · September 12, 2026 EDT**

## Objective
Separate everyday lab administration from root and protect account access before provisioning.

## Recorded implementation
Root FIDO2 hardware MFA was registered, and root Access keys (0) was verified. A separate console administrator in an Administrators group with AdministratorAccess was created; subsequent console work used that identity. Initial $100 credit availability was confirmed.

## Decisions and limits
The administrative policy is broad account-level access, not a least-privilege workload role. Application permissions were later scoped separately. A second root hardware key was explicitly deferred. Admin MFA was requested next but no explicit completion evidence was identified in the reviewed checkpoint; it is not claimed verified here.

## Validation, cost and follow-up
Root MFA assignment, zero root keys, and non-root console use were recorded. No credentials or account identifiers are published. Keep the account and budget for future labs; confirm admin MFA and backup recovery access as separate follow-up.

## Lessons
Distinguish controls visibly completed from steps merely recommended. [Completion record](../../COMPLETION-RECORD.md).
