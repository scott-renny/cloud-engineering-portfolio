# Oberon integration — planned

[Oberon](https://github.com/scott-renny/oberon) is the related AI engineering workstream for this portfolio. The repository is now verified and linked, but no deployed AWS/Oberon integration is claimed here.

The [Bedrock starter](../aws/projects/bedrock/README.md) provides an initial human-reviewed evaluation of model behavior, cloud-security advice, and inference-cost awareness. Any future Oberon cloud integration should use bounded permissions, synthetic evaluation data where practical, explicit acceptance checks, auditable actions, and cost controls.

Oberon's broader application-integration direction is API-first: it should use authorized application APIs rather than editing application databases directly. A future cloud adapter should follow the same principle.
