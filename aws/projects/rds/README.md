# Amazon Aurora PostgreSQL Serverless — completed case study
**Status: Complete · Executed: September 20, 2026 · Reward: Confirmed · Cleanup: Complete**

## Objective
Provision a minimal managed relational database, connect without a long-lived database password, execute synthetic SQL, and remove all disposable resources after validating the AWS onboarding activity.

## Architecture and configuration
AWS CloudShell → IAM database authentication → TLS → Aurora PostgreSQL Serverless writer.

- Region: `us-east-2` (Ohio)
- Cluster identifier: `aws-lab-aurora-postgres`
- Engine: Aurora PostgreSQL, server reported PostgreSQL 17.9
- Creation path: Express configuration
- Capacity: 0 ACU minimum, 4 ACU maximum, pause after 5 minutes of inactivity
- Storage: Aurora Standard
- Encryption: enabled with AWS/RDS-owned key
- Authentication: IAM only
- Database/user used for the lab: `postgres`

No account IDs, live endpoints, tokens, or credentials are published here.

## Validation
The cluster and writer both reached **Available**. AWS CloudShell's RDS console connector established an IAM-authenticated PostgreSQL session over TLS 1.3.

The first query verified the active database, database user, and server version:

```sql
SELECT current_database(), current_user, version();
```

Observed result: database `postgres`, user `postgres`, PostgreSQL 17.9.

A synthetic table was then created:

```sql
CREATE TABLE cloud_lab (
    id INTEGER GENERATED ALWAYS AS IDENTITY PRIMARY KEY,
    service VARCHAR(50) NOT NULL,
    lesson VARCHAR(200) NOT NULL,
    completed_at TIMESTAMPTZ DEFAULT CURRENT_TIMESTAMP
);
```

One synthetic row was inserted and read back successfully. This demonstrated schema creation, generated identity keys, a write, persistence, and a read. The session was closed cleanly with `\q`.

## Security decisions
IAM database authentication avoided storing a static database password for this exercise. The connection negotiated TLS 1.3. Synthetic data only was used, and no connection endpoint or authentication token was committed to Git.

Express configuration exposed an internet access gateway rather than the private-VPC design that would normally be preferred for a production workload. This was accepted only for the bounded onboarding lab and was removed immediately afterward.

## Cost and reward
The console showed metered Aurora pricing, so the lab was intentionally short-lived. After completing the activity, the AWS Console showed **$199.97 USD credits remaining**, consistent with the account's initial credit plus all five onboarding activity awards less a small amount of lab usage.

This balance is a point-in-time observation, not a claim that Aurora is free or that future usage will have no cost.

## Cleanup
The writer instance was deleted first, followed by the Aurora cluster. During cluster deletion:

- Final snapshot creation was disabled.
- Retention of automated backups was disabled.
- The console confirmed successful cluster deletion.
- Databases: **0**
- Manual snapshots: **0**
- Current Region automated backups: **0**

No disposable RDS/Aurora database, final snapshot, or retained automated backup remained after the lab.

## Lessons learned
Aurora Serverless can scale a managed PostgreSQL workload down for intermittent use, but its capacity and storage remain metered resources. IAM database authentication provides a useful alternative to long-lived database passwords. Technical completion, promotional-credit confirmation, and resource cleanup should be treated as separate acceptance checks.

This lab also reinforced a completion-first workflow: provision the smallest useful resource, validate it with real operations, capture sanitized evidence, confirm the activity outcome, and tear it down in the same session.
