# UniDash 360 — Estructura del proyecto — Sesión 1

[📘 Sesión 1](./README.md) · [⬅ Documentación](../README.md) · [🏠 UniDash 360](../../README.md) · [📚 Índice general](../../../../README.md) · [◀ Anterior](./01_RECURSOS_Y_LINKS.md) · [Siguiente ▶](./03_INDEX_HTML.md)

---

## Objetivo

Crear una estructura pequeña pero modular. La interfaz vive en `index.html`, la lógica se divide entre `modules/` y la persistencia entre `services/`.

## Estructura al terminar la sesión

```text
unidash360/
├── index.html
├── .gitignore
├── css/
│   ├── theme.css
│   └── styles.css
└── js/
    ├── app.js
    ├── modules/
    │   ├── dashboard.module.js
    │   └── tasks.module.js
    └── services/
        └── storage.service.js
```

## Responsabilidad de cada carpeta

| Ruta | Responsabilidad |
|---|---|
| `index.html` | Estructura y elementos que JavaScript manipula |
| `css/theme.css` | Variables visuales |
| `css/styles.css` | Layout y componentes |
| `js/app.js` | Arranque e integración |
| `js/modules/` | Casos de uso de la aplicación |
| `js/services/` | Acceso a mecanismos externos, inicialmente LocalStorage |

## macOS / Linux

```bash
mkdir -p unidash360/css unidash360/js/modules unidash360/js/services
cd unidash360

touch index.html .gitignore
touch css/theme.css css/styles.css
touch js/app.js
touch js/modules/dashboard.module.js
touch js/modules/tasks.module.js
touch js/services/storage.service.js
```

## Windows PowerShell

```powershell
mkdir unidash360
cd unidash360

mkdir css
mkdir js
mkdir js\modules
mkdir js\services

New-Item index.html
New-Item .gitignore
New-Item css\theme.css
New-Item css\styles.css
New-Item js\app.js
New-Item js\modules\dashboard.module.js
New-Item js\modules\tasks.module.js
New-Item js\services\storage.service.js
```

## Inicializar Git

```bash
git init
git checkout -b main
git checkout -b feature/session-01-tasks
```

## Primer commit

```bash
git add .
git commit -m "chore: create UniDash 360 project structure"
```

## Checkpoint

Antes de continuar, VS Code debe mostrar exactamente las carpetas anteriores y:

```bash
git status
```

debe indicar que no existen cambios pendientes después del commit.

---

[📘 Sesión 1](./README.md) · [⬅ Documentación](../README.md) · [🏠 UniDash 360](../../README.md) · [📚 Índice general](../../../../README.md) · [◀ Anterior](./01_RECURSOS_Y_LINKS.md) · [Siguiente ▶](./03_INDEX_HTML.md)
