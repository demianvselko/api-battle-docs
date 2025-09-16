# 🚀 Roadmap API Battle

## MVP

1. **Usuarios**
   - Registro/Login (JWT + Refresh).
   - OAuth2 con Google/Facebook.
   - Endpoint `/users/me`.

2. **Personajes**
   - Integración con PokéAPI.
   - Persistencia en MongoDB/Postgres.
   - Endpoint `/characters`.

3. **Batallas**
   - Motor 1v1 básico.
   - Historial/log de turnos.
   - Endpoint `POST /battles/1v1`.

4. **Frontend**
   - Login.
   - Selección de personaje.
   - Batalla 1v1 simple.

## Fase 2 – Ampliación de funcionalidades

- Batallas 3v3.
- Modo torneos.
- Microfrontends separados.
- Implementación de **GraphQL en el Orchestrator (ADR-0008)**.
- Sistema de progresión/niveles.

## Fase 3 – Escalabilidad y tiempo real

- Despliegue en **AWS** (ECS/EKS, RDS, DynamoDB, S3).
- **Event-driven con Kafka o AWS EventBridge (ADR-0009)**.
- Leaderboards en tiempo real.
- Modo espectador.
- Notificaciones y logs distribuidos.
