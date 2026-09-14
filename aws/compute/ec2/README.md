# Amazon EC2 — secure instance lifecycle
**Status: Complete · September 12, 2026 EDT · Instance and root EBS removed**

## Objective
Demonstrate secure provisioning, command-line administration, metadata protection, Linux validation, and deliberate teardown.

## Architecture and implementation
Windows PowerShell/OpenSSH → trusted source /32 → security group → Amazon Linux 2023 t3.micro in us-east-2 → 8-GiB encrypted gp3 root volume.

The single instance used an ED25519 key, SSH-only inbound access from the trusted public IP, no inbound HTTP/HTTPS, no instance IAM role, IMDSv2 required, Standard CPU credits, and no user data. Windows ACLs restricted the local private key. Public-key SSH succeeded.

## Security decisions and validation
| Control / check | Recorded outcome |
|---|---|
| System, instance and EBS health | Passed before SSH |
| SSH source restriction and key authentication | Authorized connection succeeded |
| Metadata without token | HTTP 401 |
| IMDSv2 token and metadata | Successful; instance details matched console |
| OS, interfaces, storage and memory | Matched intended Amazon Linux/t3.micro configuration |
| Routing, DNS and outbound HTTPS | Inspected; HTTPS response succeeded |
| Package management | DNF check completed; tree installed and verified |
| EBS | Encrypted, attached, delete-on-termination enabled |
| Teardown | Termination initiated; subsequent root-volume search returned no matching volumes |

## Troubleshooting
Windows key-path rendering caused confusion during SSH preparation. The path was verified rather than guessing or changing a working configuration. Console storage attachment naming and the guest NVMe device name were recognized as different views of the same root disk.

## Cost and cleanup
The EC2 reward was recorded as $20. Instance termination and root-volume removal closed the disposable compute/storage lifecycle. Security-group/key-pair deletion was not documented; those are not claimed removed. No exact usage charge was provided. The credit award is not a net-cost calculation.

## Lessons learned
A control is stronger portfolio evidence when its behavior is tested: requiring IMDSv2 was demonstrated with both denial and success. Teardown includes storage verification, not simply pressing Stop.

[Completion record](../../COMPLETION-RECORD.md)
