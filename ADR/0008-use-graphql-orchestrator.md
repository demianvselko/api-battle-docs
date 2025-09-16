# ADR 0008 – Uso de GraphQL en el Orchestrator

## Contexto

El frontend (web/mobile) necesita acceder a datos distribuidos en distintos microservicios: usuarios, personajes, batallas y torneos. Usar solo REST implica múltiples llamadas y riesgo de overfetching o underfetching.

## Decisión

Adoptar **GraphQL en el Orchestrator (BFF)** como capa unificada de acceso a datos.

## Justificación

- Permite a los clientes solicitar exactamente los datos necesarios.
- Reduce el número de llamadas desde frontend → un único endpoint `/graphql`.
- Provee esquema tipado, útil para autocompletado y validación en clientes.
- Encaja naturalmente en el patrón BFF, donde distintos frontends (web, mobile) tienen necesidades distintas.

## Consecuencias

- Mayor complejidad inicial en el Orchestrator (schemas, resolvers, validación de queries).
- Riesgo de queries costosas → se debe limitar la complejidad y tamaño máximo.
- Se debe documentar y versionar el schema para mantener compatibilidad.
- REST seguirá existiendo internamente entre microservicios, GraphQL será solo para frontend.
