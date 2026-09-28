# UniDash 360 — Sesión 1 completa

[📘 Sesión 1](./README.md) · [⬅ Documentación](../README.md) · [🏠 UniDash 360](../../README.md) · [📚 Índice general](../../../../README.md) · [Siguiente ▶](./01_RECURSOS_Y_LINKS.md)

---

## Dashboard + tareas + persistencia

**Duración:** 1 hora 30 minutos  
**Versión objetivo:** `v0.1.0`

## Objetivo

Construir la base de UniDash 360 con navegación responsive, un dashboard de productividad y un CRUD completo de tareas persistido en `LocalStorage`.

## Distribución sugerida

| Tiempo | Actividad |
|---|---|
| 0–10 min | Presentación del proyecto y estructura |
| 10–25 min | HTML, sidebar, dashboard y navegación |
| 25–40 min | Tema y estilos responsive |
| 40–55 min | Servicio LocalStorage |
| 55–75 min | CRUD de tareas |
| 75–85 min | Dashboard y filtros |
| 85–90 min | Validación y commit |

## Flujo

```text
Formulario
   ↓
tasks.module.js
   ↓
storage.service.js
   ↓
LocalStorage
   ↓
refreshTasks()
   ↓
Dashboard + listado
```

## Rama

```bash
git checkout -b feature/session-01-tasks
```

## Commits sugeridos

```bash
git add .
git commit -m "chore: create UniDash 360 structure"

git add .
git commit -m "feat: add responsive dashboard layout"

git add .
git commit -m "feat: add task CRUD with local storage"

git add .
git commit -m "feat: add productivity dashboard metrics"
```

## Tag

```bash
git checkout main
git merge feature/session-01-tasks
git tag -a v0.1.0 -m "UniDash 360 session 1"
```

## Criterios de cierre

- [ ] navegación funciona;
- [ ] sidebar responsive;
- [ ] crear tarea;
- [ ] editar tarea;
- [ ] completar/reabrir;
- [ ] eliminar;
- [ ] filtros;
- [ ] LocalStorage conserva datos;
- [ ] dashboard se actualiza;
- [ ] consola sin errores.

---

[📘 Sesión 1](./README.md) · [⬅ Documentación](../README.md) · [🏠 UniDash 360](../../README.md) · [📚 Índice general](../../../../README.md) · [Siguiente ▶](./01_RECURSOS_Y_LINKS.md)
