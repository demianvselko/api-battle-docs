# ADR 0005 – Estrategia de CI/CD

## Contexto

El proyecto requiere integración y despliegue continuos con validaciones automáticas.

## Decisión

Usar **GitHub Actions** para CI ligera (lint, unit tests, build) y **Jenkins** para pipelines más pesados (E2E, staging, integración).

## Justificación

- GitHub Actions:
  - Rápido feedback en PRs.
  - Configuración simple y cercana al código.
- Jenkins:
  - Poderoso para orquestar flujos complejos.
  - Integrable con AWS para despliegues.

## Consecuencias

- Doble mantenimiento de pipelines (mínimo en Actions, completo en Jenkins).
- Jenkins se usará en etapas posteriores, cuando se despliegue a AWS.
