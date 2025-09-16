# ⚔️ API Battle – Documentación Central

Este repositorio contiene la **documentación principal** del proyecto **API Battle**: visión, arquitectura, decisiones técnicas y roadmap.

## 🎯 Objetivo

Crear una plataforma de batallas entre personajes obtenidos de distintas APIs externas (PokéAPI, DigiAPI, Dragon Ball API, Marvel API, etc.), con modalidades 1v1, 3v3 y torneos.

## 📂 Contenido

- [Arquitectura](ARCHITECTURE.md)  
- [Roadmap](ROADMAP.md)  
- [ADR (Decisiones Técnicas)](ADR/)  
- [Diagramas](diagrams/)  
- [Contribución](CONTRIBUTING.md)

## 🧱 Microservicios

- `api-battle-users` → usuarios, roles, auth.  
- `api-battle-characters` → integración y persistencia de personajes.  
- `api-battle-battles` → motor de batallas.  
- `api-battle-tournaments` → lógica de torneos.  
- `api-battle-orchestrator` → BFF/fachada para frontend.  
- `api-battle-frontend` → React (microfrontends).  
- `api-battle-shared` → librerías/DTOs comunes.  
- `api-battle-infra` → infraestructura e IaC (AWS CDK).  

## 🚀 Estado Actual

- Definición de arquitectura y repositorios.  
- Documentación inicial.  
- Primer microservicio a implementar: `api-battle-users`.
