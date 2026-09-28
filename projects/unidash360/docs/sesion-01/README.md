# UniDash 360 — Sesión 1

## Dashboard, tareas y LocalStorage

**Duración:** 1 hora 30 minutos  
**Versión objetivo:** `v0.1.0`

[⬅ Documentación](../README.md) · [🏠 UniDash 360](../../README.md) · [📚 Índice general](../../../../README.md)

---

## Objetivo

Construir la base de UniDash 360 y terminar una primera versión **completamente usable**.

Al finalizar el alumno podrá:

- navegar entre Dashboard y Tareas;
- crear tareas;
- editar tareas;
- completar y reabrir tareas;
- eliminar tareas;
- filtrar por estado;
- identificar tareas vencidas;
- conservar la información después de recargar el navegador.

---

## Resultado esperado

```text
UniDash 360 v0.1.0

Dashboard
├── Total
├── Pendientes
├── Completadas
├── Vencidas
└── Próximas tareas

Tareas
├── Create
├── Read
├── Update
├── Delete
├── Filtros
└── LocalStorage
```

---

## Conceptos de la sesión

```text
DOM
Eventos
Formularios
Arrays
ES Modules
CRUD
JSON
LocalStorage
Responsive UI
Git
```

---

## Orden de documentos

| Orden | Documento | Uso |
|---:|---|---|
| 01 | [00_SESION_1_COMPLETA.md](./00_SESION_1_COMPLETA.md) | Planeación y alcance |
| 02 | [01_RECURSOS_Y_LINKS.md](./01_RECURSOS_Y_LINKS.md) | Herramientas |
| 03 | [02_ESTRUCTURA_PROYECTO.md](./02_ESTRUCTURA_PROYECTO.md) | Carpetas y Git |
| 04 | [03_INDEX_HTML.md](./03_INDEX_HTML.md) | Shell visual |
| 05 | [04_THEME_CSS.md](./04_THEME_CSS.md) | Design tokens |
| 06 | [05_STYLES_CSS.md](./05_STYLES_CSS.md) | Layout responsive |
| 07 | [06_STORAGE_SERVICE_JS.md](./06_STORAGE_SERVICE_JS.md) | Persistencia |
| 08 | [07_TASKS_MODULE_JS.md](./07_TASKS_MODULE_JS.md) | CRUD |
| 09 | [08_DASHBOARD_MODULE_JS.md](./08_DASHBOARD_MODULE_JS.md) | Métricas |
| 10 | [09_APP_JS.md](./09_APP_JS.md) | Integración |
| 11 | [10_GITIGNORE.md](./10_GITIGNORE.md) | Archivos excluidos |
| 12 | [11_PASOS_CLASE.md](./11_PASOS_CLASE.md) | Guía docente |
| 13 | [12_VALIDACION_SESION_1.md](./12_VALIDACION_SESION_1.md) | Criterios de cierre |

---

## Arquitectura de la sesión

```text
index.html
    │
    ▼
 app.js
    │
    ├───────────────┐
    ▼               ▼
tasks.module.js  dashboard.module.js
    │               │
    └──────┬────────┘
           ▼
 storage.service.js
           │
           ▼
      LocalStorage
```

---

## Rama Git

```bash
git checkout main
git checkout -b feature/session-01-tasks
```

---

## Cierre

La prueba esencial de la sesión es:

1. crear una tarea;
2. recargar el navegador;
3. comprobar que sigue apareciendo.

Si desaparece, todavía no se ha completado correctamente la persistencia.

---

[▶ Comenzar Sesión 1](./00_SESION_1_COMPLETA.md)
