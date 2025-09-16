# 🤝 Contribuyendo a API Battle

Gracias por tu interés en contribuir 🚀.  
Este documento define las reglas y guías para colaborar en **API Battle**.

---

## 🔧 Requisitos previos

- Node.js LTS (>=18)
- npm o yarn
- Docker (para DB y entorno local)
- Jenkins (para pipelines de CI/CD)
- SonarQube (para análisis de calidad de código)

---

## 📦 Estilo de código

- **ESLint + Prettier** → consistencia en estilo.
- **Commitlint** → convenciones de commits.
- **Husky + lint-staged** → validación de commits antes de hacer push.

---

## 🧪 Testing

### Librerías

- **Jest** → unit tests.
- **Supertest** → integración (APIs).
- **Cypress/Playwright** → E2E.
- **SonarQube** → cobertura y calidad de código.

### Local

```bash
# Instalar dependencias
npm install

# Levantar servicios necesarios (ej: DB)
docker-compose up -d db

# Correr unit tests
npm run test

# Correr tests con cobertura
npm run test:coverage

# Correr tests E2E
npm run test:e2e


⚠️ Nota: si es tu primera vez, asegúrate de copiar variables de entorno desde .env.example a .env.

```

## 📦 Estilo de código

ESLint + Prettier → consistencia en el código.

Commitlint → convenciones de commits (Conventional Commits).

Husky + lint-staged → validación de código antes del commit.

## 🔀 Flujo de trabajo

- Haz fork o crea una rama desde `main`.
- Usa nombres de ramas descriptivas:
  - `feature/auth-login` → Nueva funcionalidad
  - `fix/battle-draw-condition` → Corrección de bug
  - `hotfix/login-bug` → Urgente en producción

- Realiza commits siguiendo la convención.

- Haz PR hacia `main` asegurándote de:
  - ✅ Linter debe pasar.
  - ✅ Tests deben estar en verde.
  - ✅ Análisis de SonarQube sin blockers.
  - 👀 Otro colaborador debe aprobar antes del merge.

## 📄 Convención de commits

Usamos **[Conventional Commits](https://www.conventionalcommits.org/)** para mantener un historial consistente y legible.

### 📝 Formato

### ✅ Tipos permitidos

- **feat** → nueva funcionalidad  
- **fix** → corrección de bug  
- **hotfix** → corrección urgente en producción  
- **refactor** → cambio de código sin alterar funcionalidad  
- **test** → agregar o corregir tests  
- **docs** → cambios en documentación  
- **chore** → tareas varias (dependencias, config)  
- **style** → cambios de formato/código (sin impacto funcional)  
- **perf** → mejoras de rendimiento  
- **ci** → cambios en configuración de CI/CD  
- **build** → cambios en build, dependencias, paquetes  

### 💡 Ejemplos

- `feat(auth): add JWT refresh token`
- `fix(battles): correct powerLevel calculation`
- `hotfix(users): patch OAuth2 callback issue`
- `refactor(characters): simplify stats mapper`
- `test(battles): add unit test for draw condition`
- `docs(roadmap): update phase 2 with GraphQL`
- `chore(deps): update NestJS to v10`
- `ci(jenkins): add SonarQube integration`

## 📊 Calidad y Análisis Estático

Cada PR debe pasar por **SonarQube** y cumplir con estas condiciones antes de poder mergear:

- 🚫 **Sin Blocker issues** → errores críticos o de seguridad que comprometen la ejecución.  
- 🚫 **Sin Critical issues** → vulnerabilidades o bugs severos.  
- ⚠️ Los **Major issues** deben revisarse y resolverse antes de mergear, salvo justificación documentada.  
- ℹ️ Los **Minor** e **Info** pueden quedar abiertos, pero se recomienda atenderlos en el ciclo de mantenimiento.

🔒 **El merge estará bloqueado automáticamente si existen Blocker o Critical issues.**

- Jenkins integrará el análisis Sonar y publicará reportes.

## 📢 Comunicación

- Issues → bugs y nuevas propuestas.

- Pull Requests → contribuciones de código.

- ADR → decisiones técnicas documentadas en /ADR.

### ✅ Siguiendo estas guías aseguramos un código mantenible, consistente y de calidad en todo el ecosistema de API Battle, no la cagues
