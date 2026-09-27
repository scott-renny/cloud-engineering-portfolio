# Oberon integration — planned

Oberon is a related personal AI-assistant engineering workstream. It remains a private repository for now, so no link is published here; no deployed AWS/Oberon integration is claimed.

The [Bedrock starter](../aws/projects/bedrock/README.md) provides an initial human-reviewed evaluation of model behavior, cloud-security advice, and inference-cost awareness. Any future Oberon cloud integration should use bounded permissions, synthetic evaluation data where practical, explicit acceptance checks, auditable actions, and cost controls.

Oberon's broader application-integration direction is API-first: it should use authorized application APIs rather than editing application databases directly. A future cloud adapter should follow the same principle.
