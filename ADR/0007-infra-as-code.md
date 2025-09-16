# ADR 0007 – Infraestructura como Código

## Contexto

Se necesita definir cómo se gestionará la infraestructura en AWS. Las opciones eran Terraform y AWS CDK.

## Decisión

Adoptar **AWS CDK** como herramienta de IaC.

## Justificación

- CDK:
  - Permite usar TypeScript (alineado al stack principal del proyecto).
  - Integración nativa con servicios de AWS.
  - Curva de aprendizaje menor para el equipo.
- Terraform se descarta por ahora, aunque es estándar multi-cloud.

## Consecuencias

- Dependencia directa del ecosistema AWS.
- Aumenta la productividad inicial gracias a TypeScript.
- Se centralizará en un repo `api-battle-infra`.
