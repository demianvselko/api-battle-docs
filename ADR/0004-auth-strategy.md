# ADR 0004 – Estrategia de Autenticación

## Contexto

El sistema debe autenticar usuarios registrados y visitantes, soportando además login social.

## Decisión

Adoptar **JWT + Refresh Token** como base, con soporte adicional para **OAuth2 (Google, Facebook)**.

## Justificación

- JWT:
  - Simple de manejar en microservicios y escalable.
  - Compatible con API Gateway y BFF.
- Refresh Token:
  - Mejora la seguridad al renovar accesos sin pedir credenciales.
- OAuth2:
  - Facilita acceso con redes sociales.
  - Menor fricción para usuarios nuevos.

## Consecuencias

- Requiere un microservicio de usuarios robusto (`api-battle-users`).
- Tokens deben ser validados en API Gateway/BFF.
- Se debe implementar un sistema seguro de almacenamiento/rotación de refresh tokens.
