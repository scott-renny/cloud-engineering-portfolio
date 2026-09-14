# Amazon Bedrock — human-reviewed cloud security analysis
**Status: Complete · September 13, 2026 UTC · Two requests; no persistent deployment**

## Objective and architecture
Evaluate a foundation model's advice against an EC2 configuration already validated by the operator.
Bedrock chat playground → Amazon Nova Micro 1.0 → US Nova Micro cross-region inference profile → human review.

## Implementation
The initial prompt described Amazon Linux 2023, t3.micro, encrypted EBS, restricted SSH, key authentication, required IMDSv2, and no web ingress. A second prompt explicitly asked for recommendations that were not already implemented and clarified account access versus SSH.

## Validation and security decisions
The first request reported 82 input tokens, 162 output tokens, and 712 ms. Across both requests, the recorded counters totaled 392 input and 418 output tokens.

The first answer identified several real strengths but repeated an existing SSH restriction, confused the relevance of MFA to the SSH path, and missed IMDSv2. After correction, the answer became more relevant but still needed review, particularly its description of NACL scope and the cost/complexity of additional services. No model recommendation was automatically applied.

## Troubleshooting and lessons
Prompt refinement improved relevance without making the answer authoritative. The useful outcome was the review process: compare advice to the actual configuration, reject redundant suggestions, and consider operational cost before adopting a control.

## Cost and cleanup
The onboarding summary showed Bedrock completed and $60 total additional credits across three activities. Both requests ended; no provisioned throughput, dedicated endpoint, knowledge base, or agent was created. Exact billed inference cost was not supplied.

This exercise is separate from the Help Desk's planned v0.3 AI assistant and the future Oberon integration.

[Completion record](../../COMPLETION-RECORD.md)
