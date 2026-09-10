# BeatFlow — Sesión 1
## UI/UX, estructura y layout responsive

**Duración:** 1 hora 30 minutos  
**Versión objetivo:** `v0.1.0`

## Objetivo

Construir la primera versión visual de BeatFlow utilizando únicamente:

- HTML5
- TailwindCSS mediante CDN
- JavaScript ES Modules
- Datos mock
- Git

En esta sesión **no se conecta ninguna API** y **no se reproduce audio real**.

---

## Resultado esperado

Al terminar la sesión debe existir una interfaz funcional con:

- Sidebar para escritorio
- Header
- Buscador visual
- Hero principal
- Sección de tendencias
- Cards de canciones
- Sección de escuchados recientemente
- Player visual fijo
- Navegación inferior para móvil
- Layout responsive

---

## Estructura del proyecto

```text
beatflow/
├── index.html
├── assets/
│   └── images/
│       └── README.md
└── js/
    ├── app.js
    ├── data/
    │   └── mock.data.js
    └── ui/
        └── home.ui.js
```

---

## Flujo de trabajo

```text
Datos mock
   ↓
mock.data.js
   ↓
home.ui.js
   ↓
renderHome()
   ↓
DOM
```

---

## Rama sugerida

```bash
git checkout -b feature/ui-layout
```

## Commits sugeridos

```bash
git add .
git commit -m "feat: create BeatFlow base layout"
```

```bash
git add .
git commit -m "feat: add responsive sidebar navigation"
```

```bash
git add .
git commit -m "feat: add track card component"
```

```bash
git add .
git commit -m "feat: add desktop music player"
```

```bash
git add .
git commit -m "feat: add mobile navigation"
```

---

## Tag de versión

```bash
git tag -a v0.1.0 -m "BeatFlow session 1"
```

---

## Checklist

- [ ] El proyecto abre correctamente en navegador
- [ ] No existen errores en consola
- [ ] El sidebar se oculta en móvil
- [ ] La navegación inferior aparece en móvil
- [ ] Las cards se adaptan a diferentes resoluciones
- [ ] El player permanece visible
- [ ] Las canciones se generan desde JavaScript
- [ ] No existen secretos o API Keys
- [ ] Los commits son pequeños y descriptivos
