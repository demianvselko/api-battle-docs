# ADR 0009 – Event-Driven con Kafka (futuro)

## Contexto

El sistema manejará flujos en tiempo real: batallas, torneos, logs y estadísticas. REST es suficiente para MVP, pero no escala bien para comunicación asíncrona y auditoría.

## Decisión

Adoptar un enfoque **event-driven** con **Kafka** (o alternativa como AWS EventBridge/NATS) en una fase futura, una vez validado el MVP.

## Justificación

- Kafka:
  - Alta escalabilidad y throughput.
  - Persistencia de eventos → replays, auditoría, debugging.
  - Desacopla productores y consumidores.
- Útil para: “batalla iniciada”, “turno completado”, “torneo finalizado”, logs de auditoría.

## Consecuencias

- Complejidad operativa alta (clusters, particiones, monitoring).
- No será parte del MVP inicial, se evaluará cuando se necesite escalabilidad y tiempo real.
- Requiere diseñar contratos de eventos (topics, payloads, versionado).
- REST seguirá siendo la interfaz principal en MVP, Kafka será un complemento futuro.
