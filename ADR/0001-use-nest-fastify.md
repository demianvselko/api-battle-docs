# ADR 0001 – Uso de NestJS con Fastify

## Contexto

Se necesitaba definir el framework base para los microservicios del backend. Las opciones principales eran Express, NestJS con Express y NestJS con Fastify.

## Decisión

Adoptar **NestJS con Fastify** en todos los microservicios.

## Justificación

- NestJS:
  - Soporte nativo a inyección de dependencias.
  - Modularidad y estructura clara para arquitectura hexagonal.
  - Ecosistema sólido (CLI, Swagger, testing).
- Fastify:
  - Mayor rendimiento que Express.
  - Soporte nativo de JSON Schema.
  - Ecosistema de plugins modernos.

## Consecuencias

- Uniformidad en todos los servicios.
- Curva de aprendizaje inicial un poco mayor, pero mejor mantenibilidad.
- Integración sencilla con Jest y herramientas de CI.
