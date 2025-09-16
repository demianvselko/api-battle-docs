# 🧱 Arquitectura API Battle

## Backend

- **Arquitectura Hexagonal** en cada microservicio.  
- **NestJS + Fastify** como framework base.  
- **Comunicación**: REST (inicial), gRPC/EventBus (futuro).  
- **Persistencia**:
  - SQL (Postgres) → usuarios, torneos, batallas.
  - NoSQL (MongoDB/DynamoDB) → personajes y estadísticas dinámicas.
- **Autenticación**: JWT + Refresh Token, OAuth2 (Google, Facebook).

## Frontend

- **React** con Webpack Module Federation.  
- Mobile-first, posible PWA.  
- Microfrontends: Auth, Characters, Battle, Tournaments.

## Infraestructura

- **Docker** para dev.  
- **CI/CD** con GitHub Actions + Jenkins.  
- **Infraestructura como Código** (Terraform o AWS CDK).  
- Despliegue futuro en **AWS** (ECS/EKS, RDS, DynamoDB, S3).

## Diagramas

Consulta los diagramas en [`/diagrams`](diagrams).

---
