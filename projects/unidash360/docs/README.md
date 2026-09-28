# UniDash 360 — Documentación

Este directorio contiene la guía completa para desarrollar **UniDash 360** en tres sesiones evolutivas.

[🏠 UniDash 360](../README.md) · [📚 Índice general](../../../README.md)

---

## Índice de sesiones

| Sesión | Tema | Versión | Resultado |
|---:|---|---|---|
| 1 | [Dashboard, tareas y LocalStorage](./sesion-01/README.md) | `v0.1.0` | CRUD persistente |
| 2 | [Finanzas, métricas y Chart.js](./sesion-02/README.md) | `v0.2.0` | Analítica financiera |
| 3 | [Ubicación, clima, divisas y noticias](./sesion-03/README.md) | `v1.0.0` | Dashboard conectado a APIs |

---

## Flujo del proyecto

```text
SESIÓN 1
Dashboard + Tareas + LocalStorage
                │
                ▼
             v0.1.0
                │
                ▼
SESIÓN 2
Finanzas + Agregaciones + Chart.js
                │
                ▼
             v0.2.0
                │
                ▼
SESIÓN 3
Geolocation + Weather + FX + News
                │
                ▼
             v1.0.0
```

---

## Forma de trabajo

Cada sesión se realiza en orden.

La guía separa:

```text
README.md
     │
     ├── objetivo
     ├── resultado esperado
     ├── orden de documentos
     ├── arquitectura
     ├── código completo
     ├── pasos de clase
     ├── Git
     └── validación
```

Cuando una sesión modifica un archivo existente, el documento correspondiente presenta **el archivo completo resultante**, no únicamente fragmentos.

Los archivos que no aparecen en una sesión se conservan tal como terminaron en la sesión anterior.

---

## Recomendación para el alumno

Antes de empezar una nueva sesión:

```bash
git status
```

Debe mostrar el repositorio limpio.

Después:

```bash
git checkout main
git pull
```

y crear la rama indicada por la guía.

---

## Comenzar

[▶ Iniciar Sesión 1](./sesion-01/README.md)

---

[🏠 UniDash 360](../README.md) · [📚 Índice general](../../../README.md)
