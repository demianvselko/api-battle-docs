# ADR 0006 – Comunicación entre Microservicios

## Contexto

Los microservicios deben interactuar entre sí para coordinar batallas, usuarios y torneos.

## Decisión

- **Fase inicial**: comunicación vía **REST** (HTTP/JSON).  
- **Fase futura**: transición hacia arquitectura **event-driven** con un bus de eventos (ej: AWS EventBridge, Kafka, NATS).

## Justificación

- REST: sencillo de implementar, rápido de prototipar, herramientas maduras.  
- Event-driven: escalable, desacoplado, mejor para auditoría y seguimiento de batallas/torneos.  

## Consecuencias

- Se requiere diseñar DTOs y contratos claros desde el inicio.
- A futuro, los microservicios deberán emitir eventos además de exponer endpoints.
- Se evaluará añadir un `api-battle-shared` con definiciones comunes.
