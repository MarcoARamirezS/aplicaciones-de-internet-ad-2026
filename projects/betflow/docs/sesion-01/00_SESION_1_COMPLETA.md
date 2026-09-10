# BeatFlow — Sesión 1

## UI/UX, estructura y layout responsive

**Duración:** 1 hora 30 minutos  
**Versión objetivo:** `v0.1.0`

[⬅ Documentación](../README.md) · [🏠 BeatFlow](../../README.md) · [📚 Índice general](../../../../README.md)

---

## Índice

- [Objetivo](#objetivo)
- [Resultado esperado](#resultado-esperado)
- [Estructura del proyecto](#estructura-del-proyecto)
- [Flujo de trabajo](#flujo-de-trabajo)
- [Rama sugerida](#rama-sugerida)
- [Commits sugeridos](#commits-sugeridos)
- [Tag de versión](#tag-de-versión)
- [Checklist](#checklist)
- [Siguiente documento](#siguiente-documento)

---

## Objetivo

Construir la primera versión visual de BeatFlow utilizando únicamente:

- HTML5
- TailwindCSS mediante CDN
- CSS separado
- JavaScript ES Modules
- Datos mock
- Git

En esta sesión **no se conecta ninguna API**, **no se reproduce audio real** y **no se utiliza LocalStorage**.

El objetivo es establecer una base visual, responsive y modular que pueda evolucionar durante las siguientes sesiones sin rehacer la arquitectura del proyecto.

[⬆ Regresar al índice](#índice)

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
- Datos mock
- JavaScript modular
- Estados visuales básicos

La versión obtenida al finalizar será:

```text
BeatFlow v0.1.0
```

[⬆ Regresar al índice](#índice)

---

## Estructura del proyecto

Al concluir la Sesión 1, la parte ejecutable del proyecto debe quedar:

```text
beatflow/
│
├── README.md
├── index.html
├── .gitignore
│
├── css/
│   ├── theme.css
│   └── styles.css
│
├── assets/
│   └── images/
│
├── js/
│   ├── app.js
│   │
│   ├── data/
│   │   └── mock.data.js
│   │
│   └── ui/
│       └── home.ui.js
│
└── docs/
    ├── README.md
    │
    └── sesion-01/
        ├── README.md
        ├── 00_SESION_1_COMPLETA.md
        ├── 01_RECURSOS_Y_LINKS.md
        ├── 02_ESTRUCTURA_PROYECTO.md
        ├── 03_INDEX_HTML.md
        ├── 04_THEME_CSS.md
        ├── 05_STYLES_CSS.md
        ├── 06_MOCK_DATA_JS.md
        ├── 07_HOME_UI_JS.md
        ├── 08_APP_JS.md
        ├── 09_GITIGNORE.md
        ├── 10_README.md
        ├── 11_PASOS_CLASE.md
        └── 12_VALIDACION_SESION_1.md
```

### Responsabilidad de los archivos principales

| Archivo | Responsabilidad |
|---|---|
| `index.html` | Estructura principal de la interfaz |
| `css/theme.css` | Design Tokens e identidad visual |
| `css/styles.css` | Estilos globales y complementarios |
| `js/data/mock.data.js` | Datos musicales simulados |
| `js/ui/home.ui.js` | Render dinámico de Home |
| `js/app.js` | Estado, navegación y eventos |
| `.gitignore` | Exclusión de archivos que no deben versionarse |
| `README.md` | Documentación principal de BeatFlow |

[⬆ Regresar al índice](#índice)

---

## Flujo de trabajo

La Sesión 1 utiliza información simulada.

```text
Datos mock
    │
    ▼
mock.data.js
    │
    ▼
app.js
    │
    ▼
home.ui.js
    │
    ▼
renderHome()
    │
    ▼
DOM
    │
    ▼
Usuario
```

Conceptualmente:

```text
DATA
  ↓
STATE
  ↓
RENDER
  ↓
DOM
```

En esta sesión todavía no existe:

```text
REST API
Audio real
LocalStorage
Autenticación
Backend
```

[⬆ Regresar al índice](#índice)

---

## Rama sugerida

Para mantener consistencia con el resto del proyecto se recomienda:

```bash
git checkout -b feature/session-01-ui
```

Verificar la rama:

```bash
git branch
```

Resultado esperado:

```text
* feature/session-01-ui
  main
```

[⬆ Regresar al índice](#índice)

---

## Commits sugeridos

Los commits deben realizarse conforme avance la implementación, no todos al final.

### 1. Estructura del proyecto

```bash
git add .
git commit -m "chore: create BeatFlow project structure"
```

### 2. Layout principal

```bash
git add .
git commit -m "feat: create BeatFlow base layout"
```

### 3. Sidebar responsive

```bash
git add .
git commit -m "feat: add responsive sidebar navigation"
```

### 4. Theme y estilos globales

```bash
git add .
git commit -m "style: add BeatFlow theme and global styles"
```

### 5. Datos mock

```bash
git add .
git commit -m "feat: add mock music data"
```

### 6. Cards

```bash
git add .
git commit -m "feat: add track card component"
```

### 7. Player visual

```bash
git add .
git commit -m "feat: add desktop music player"
```

### 8. Navegación móvil

```bash
git add .
git commit -m "feat: add mobile navigation"
```

### Revisar historial

```bash
git log --oneline
```

[⬆ Regresar al índice](#índice)

---

## Tag de versión

Una vez que la sesión esté completamente validada, regresar a `main`:

```bash
git checkout main
```

Integrar la rama:

```bash
git merge feature/session-01-ui
```

Crear el tag:

```bash
git tag -a v0.1.0 -m "BeatFlow session 1"
```

Verificar:

```bash
git tag
```

Resultado esperado:

```text
v0.1.0
```

Opcionalmente, si el repositorio remoto ya está configurado:

```bash
git push origin main
git push origin v0.1.0
```

[⬆ Regresar al índice](#índice)

---

## Checklist

### Ejecución

- [ ] El proyecto abre correctamente en navegador
- [ ] Se ejecuta mediante un servidor local
- [ ] TailwindCSS carga correctamente
- [ ] `theme.css` carga correctamente
- [ ] `styles.css` carga correctamente
- [ ] No existen errores en consola

### UI/UX

- [ ] El sidebar se muestra en escritorio
- [ ] El sidebar se oculta en móvil
- [ ] La navegación inferior aparece en móvil
- [ ] El Header se adapta correctamente
- [ ] El Hero responde a distintos tamaños
- [ ] Las cards se adaptan a diferentes resoluciones
- [ ] El player permanece visible
- [ ] Existe focus visible para navegación por teclado

### JavaScript

- [ ] Las canciones se generan desde JavaScript
- [ ] Los datos mock están separados de la UI
- [ ] `home.ui.js` se encarga del render
- [ ] `app.js` coordina estado y eventos
- [ ] El botón Play cambia visualmente
- [ ] No se intenta reproducir audio real todavía

### Responsive

Probar al menos:

```text
375px
768px
1024px
1440px
```

### Seguridad

- [ ] No existen secretos
- [ ] No existen API Keys
- [ ] `.env` está contemplado en `.gitignore`

### Git

- [ ] Se trabajó en `feature/session-01-ui`
- [ ] Los commits son pequeños y descriptivos
- [ ] La rama fue integrada a `main`
- [ ] Existe el tag `v0.1.0`

Para la revisión detallada utilizar:

[✅ 12_VALIDACION_SESION_1.md](./12_VALIDACION_SESION_1.md)

[⬆ Regresar al índice](#índice)

---

## Siguiente documento

Una vez comprendido el alcance de la sesión, continuar con los recursos necesarios:

[➡ 01_RECURSOS_Y_LINKS.md](./01_RECURSOS_Y_LINKS.md)

Después seguir el orden establecido en:

[📘 README de la Sesión 1](./README.md)

---

## Navegación

[⬅ Documentación](../README.md) · [🏠 BeatFlow](../../README.md) · [📚 Índice general](../../../../README.md)

[⬆ Regresar al índice](#índice)

[➡ Siguiente: Recursos y links](./01_RECURSOS_Y_LINKS.md)
