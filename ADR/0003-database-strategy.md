# ADR 0003 – Estrategia de Bases de Datos (SQL + NoSQL)

## Contexto

El sistema requiere almacenar datos con naturalezas diferentes:  

- Usuarios, torneos y batallas → datos estructurados y relacionales.  
- Personajes → datos dinámicos, provenientes de APIs externas y con cambios frecuentes.

## Decisión

Adoptar un enfoque **híbrido**:

- **Postgres** (SQL) → usuarios, roles, torneos, batallas.
- **MongoDB/DynamoDB** (NoSQL) → personajes y estadísticas dinámicas.

## Justificación

- SQL: ideal para relaciones, integridad referencial y consultas complejas (torneos, usuarios).  
- NoSQL: mayor flexibilidad y escalabilidad para datos heterogéneos (personajes, stats).  
- La arquitectura hexagonal permite abstraer la persistencia, facilitando cambios futuros.

## Consecuencias

- Complejidad añadida en la gestión de dos motores de base de datos.
- Se necesitarán conectores diferentes en cada microservicio.
- Escalabilidad y performance más adecuadas a cada tipo de dato.
