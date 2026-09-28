# UniDash 360 — Pasos de clase — Sesión 1

[📘 Sesión 1](./README.md) · [⬅ Documentación](../README.md) · [🏠 UniDash 360](../../README.md) · [📚 Índice general](../../../../README.md) · [◀ Anterior](./10_GITIGNORE.md) · [Siguiente ▶](./12_VALIDACION_SESION_1.md)

---

## 0–10 min — Presentación

Explicar el objetivo:

```text
datos propios
    ↓
LocalStorage
    ↓
Dashboard
```

Mostrar el resultado final que se busca al cierre de la sesión.

---

## 10–20 min — Estructura

1. Crear carpetas.
2. Inicializar Git.
3. Crear la rama `feature/session-01-tasks`.
4. Abrir la carpeta en VS Code.
5. Iniciar Live Server.

Checkpoint:

```text
index.html abre mediante localhost
sin errores rojos en Console
```

---

## 20–35 min — UI

Crear:

```text
index.html
css/theme.css
css/styles.css
```

Explicar:

- sidebar;
- vistas mediante `section`;
- `data-view`;
- IDs que JavaScript utilizará;
- responsive design.

Checkpoint:

- Dashboard visible.
- Vista Tareas visible mediante navegación.
- Menú móvil abre y cierra.

---

## 35–48 min — LocalStorage

Crear:

```text
js/services/storage.service.js
```

Explicar:

```javascript
JSON.stringify()
JSON.parse()
localStorage.setItem()
localStorage.getItem()
```

Abrir:

```text
DevTools
→ Application
→ Local Storage
```

Identificar:

```text
unidash360.tasks
```

---

## 48–72 min — CRUD de tareas

Crear:

```text
js/modules/tasks.module.js
```

Probar en este orden:

1. crear;
2. listar;
3. completar;
4. reabrir;
5. editar;
6. eliminar;
7. filtrar.

Relacionar cada acción con:

```text
Create
Read
Update
Delete
```

Checkpoint:

crear una tarea y verla inmediatamente sin recargar la página.

---

## 72–82 min — Dashboard

Crear:

```text
js/modules/dashboard.module.js
```

Actualizar:

```text
js/app.js
```

Validar:

- total;
- pendientes;
- completadas;
- vencidas;
- próximas tareas.

---

## 82–90 min — Persistencia y Git

1. Crear una tarea.
2. Recargar.
3. Confirmar que permanece.
4. Revisar Console.
5. Ejecutar:

```bash
git status
git add .
git commit -m "feat: add task CRUD with local storage"
```

Al finalizar la sesión ejecutar la validación formal del documento `12_VALIDACION_SESION_1.md`.

---

[📘 Sesión 1](./README.md) · [⬅ Documentación](../README.md) · [🏠 UniDash 360](../../README.md) · [📚 Índice general](../../../../README.md) · [◀ Anterior](./10_GITIGNORE.md) · [Siguiente ▶](./12_VALIDACION_SESION_1.md)
