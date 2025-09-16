# ADR 0002 – Estrategia Multirepo vs Monorepo

## Contexto

El proyecto requiere varios bounded contexts (users, characters, battles, tournaments, frontend, etc.). La discusión estaba entre concentrar todo en un monorepo o dividir en múltiples repositorios.

## Decisión

Adoptar un enfoque **multirepo**: cada bounded context tendrá su propio repositorio.

## Justificación

- Escalabilidad organizacional: equipos pueden trabajar de forma independiente.
- Despliegue desacoplado: cada microservicio puede tener su pipeline y release cycle.
- Simplicidad en CI/CD: pipelines más rápidos y específicos.
- Claridad en ownership: cada repo tiene responsables claros.

## Consecuencias

- Más esfuerzo inicial en la organización de repositorios.
- Se requerirá un repositorio central de documentación (`api-battle-docs`).
- Coordinación extra para cambios que impacten a varios servicios (se mitiga con `api-battle-shared`).
