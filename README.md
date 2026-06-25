# Documentación — WebLandingSuite

> Repositorio oficial de documentación del proyecto **WebLandingSuite**, desarrollado en el marco de la asignatura **Taller Aplicado de Programación (TPY1101) · Sección 001D** — Duoc UC.

---

## Integrantes — Grupo N°6

| Nombre | Rol |
|--------|-----|
| Juan Carlos Agüero Carcamo | Desarrollador |
| Rene Marcos Antonio Orellana Aguirre | Desarrollador |
| Isaac Amaru Gonzalez Saavedra | Desarrollador |

**Docente:** Cristian M. Calderón Sánchez

---

## Descripción del Proyecto

**WebLandingSuite** es una plataforma web SaaS que permite a usuarios no técnicos generar, personalizar y descargar landing pages profesionales de forma automatizada mediante inteligencia artificial.

El sistema integra tres componentes principales:

- **Frontend React** — Interfaz SPA con formulario multi-paso para configuración de la landing.
- **Backend Spring Boot** — Núcleo del sistema con autenticación JWT, lógica de negocio y orquestación de servicios.
- **API Python (FastAPI)** — Motor de generación de contenido HTML mediante modelos de IA según plan contratado.

---

## Arquitectura General

```
Usuario
  └── Frontend React (Vercel)
          └── Backend Spring Boot (Render)
                  ├── PostgreSQL Neon DB
                  ├── Cloudinary (imágenes)
                  ├── Resend (correos)
                  └── API Python FastAPI (Render)
                            └── OpenRouter AI
                                    ├── BASIC      → google/gemini-2.5-flash-lite
                                    ├── INTERMEDIATE → openai/gpt-4o-mini
                                    └── PREMIUM    → anthropic/claude-haiku-4.5
```

---

## Repositorios del Proyecto

| Componente | Repositorio | Tecnología |
|------------|-------------|------------|
| Frontend | [WLSuiteFrontend](https://github.com/Amaaruu/WLSuiteFrontend) | React 19 + Vite + Tailwind |
| Backend | [Landingbackend](https://github.com/Amaaruu/Landingbackend) | Spring Boot 3.2.5 + JUnit 5 |
| API IA | [WLSuitePythonAPI](https://github.com/Amaaruu/WLSuitePythonAPI) | FastAPI + pytest |

---

## Estructura del Repositorio

```
Documentacion-WebLanding.suite/
│
├── Documentacion/
│   ├── Informe - EA3 - Taller de Programación.pdf
│   ├── BD WebLandingSuite.pdf
│   ├── Carta Gantt.xlsx
│   ├── Casos de Uso WlS Final.pdf
│   ├── Diagrama de Arquitectura.pdf
│   ├── Diagrama de arbol de problema.pdf
│   ├── Diagrama de contenedores nivel 1.pdf       ← C4 Nivel 1
│   ├── Diagrama de contenedor nivel2.pdf           ← C4 Nivel 2
│   ├── Situacion Inicial del Cliente - Proceso Actual (AS-IS).pdf
│   ├── Solucion TO BE - WebLandingSuite.pdf
│   │
│   ├── Evidencia Backend Test/
│   │   ├── Ejecutar Suite de Regresion.pdf
│   │   ├── Ejecutar todas las pruebas (Unitarias e Integracion).pdf
│   │   ├── Ejecutar una clase de prueba especifica LandingProjectServiceTest.pdf
│   │   ├── Generacion de reporte de Cobertura (JaCoCo).pdf
│   │   ├── Pruebas de Rendimiento y carga (Gatling).pdf
│   │   ├── Pruebas de Rendimiento y carga 1.pdf
│   │   ├── Pruebas de Rendimiento y carga 2.pdf
│   │   ├── Pruebas de Rendimiento y carga 3.pdf
│   │   ├── Pruebas de rendimiento y carga (Terminal).pdf
│   │   ├── Reporte generado (session).pdf
│   │   ├── Reporte generado.pdf
│   │   └── Test de seguridad.pdf
│   │
│   ├── Evidencia Frontend Test/
│   │   ├── Ejecucion de pruebas E2E (Playwright).pdf
│   │   ├── Pruebas Unitarias y Cobertura (Vitest).pdf
│   │   ├── Reporte de las pruebas Unitarias y Cobertura (Vitest).pdf
│   │   ├── Reporte detallado de Playwright.pdf
│   │   └── SecurityEndpointsTest.pdf
│   │
│   └── Evidencia API Python Test/
│       └── Evidencia de Cobertura (Coverage).pdf
│
├── Gestion/
│   └── 1.1.2 Documento de registro de definición e identificación del proyecto.docx
│
├── Producto/
│   ├── Descripcion_producto.txt
│   ├── Landingbackend-main.zip
│   ├── WLSuiteFrontend-main.zip
│   └── WLSuitePythonAPI-main.zip
│
└── Integrantes.txt
```

---

## Resumen de Pruebas Aplicadas

| Capa | Tipo de Prueba | Herramienta | Cobertura / Resultado |
|------|---------------|-------------|----------------------|
| Backend | Unitarias + Integración | JUnit 5 + Testcontainers | 139 tests / JaCoCo gate 90% |
| Backend | Rendimiento y Carga | Gatling 3.11.3 | Reportes incluidos |
| Backend | Seguridad | OWASP | Evidencia incluida |
| Backend | Regresión | JUnit 5 | Suite completa |
| Frontend | Unitarias + Cobertura | Vitest 4.1.9 | 91.66% cobertura |
| Frontend | End-to-End | Playwright 1.61 | 3 pruebas passed |
| Frontend | Seguridad Endpoints | Playwright | Evidencia incluida |
| API Python | Unitarias + Cobertura | pytest + Coverage | 97% cobertura |

---

## Stack Tecnológico y Despliegue

| Componente | Plataforma | Tecnología |
|------------|-----------|------------|
| Frontend | Vercel | React 19, Vite, Tailwind CSS, React Router v7 |
| Backend | Render (Docker) | Spring Boot 3.2.5, Java 21, JWT, JPA |
| API IA | Render | FastAPI, Python, OpenRouter |
| Base de Datos | Neon (PostgreSQL) | PostgreSQL serverless |
| Imágenes | Cloudinary | Almacenamiento cloud |
| Correos | Resend | Transaccional |
| Monitoreo | UptimeRobot | Disponibilidad |
| CI/CD | GitHub Actions | Coverage gate automatizado |

---

## Documentos Principales

| Documento | Descripción |
|-----------|-------------|
| Informe EA3 | Informe técnico completo de la evaluación 3 |
| Carta Gantt | Planificación del proyecto por fases |
| Diagrama de Arquitectura | Vista general del sistema |
| Diagramas C4 (Nivel 1 y 2) | Contexto y contenedores del sistema |
| BD WebLandingSuite | Modelo entidad-relación de la base de datos |
| Casos de Uso | Casos de uso por módulo |
| AS-IS | Situación inicial del cliente (proceso actual) |
| TO-BE | Solución propuesta con WebLandingSuite |

---

## Notas

- Todos los repositorios de código fuente se encuentran en **modo público**.
- El código fuente de cada componente está disponible en la carpeta `Producto/` en formato `.zip` correspondiente a la rama `main`.
- El documento de gestión `1.1.2` corresponde a la primera entrega del proyecto.

---

*Taller Aplicado de Programación · TPY1101 · Sección 001D · Duoc UC · 2026*
