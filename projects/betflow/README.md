# BeatFlow

Aplicación web musical desarrollada como proyecto evolutivo para la materia **Aplicaciones de Internet**.

BeatFlow está inspirado en la experiencia de plataformas modernas de streaming musical, pero utiliza una identidad visual propia y un stack deliberadamente simple para reforzar fundamentos de desarrollo frontend.

---

## Índice

- [Objetivo del proyecto](#objetivo-del-proyecto)
- [Stack tecnológico](#stack-tecnológico)
- [Restricciones del proyecto](#restricciones-del-proyecto)
- [Estructura general](#estructura-general)
- [Arquitectura conceptual](#arquitectura-conceptual)
- [Roadmap](#roadmap)
- [Sesiones](#sesiones)
  - [Sesión 1 — UI/UX y estructura](#sesión-1--uiux-y-estructura)
  - [Sesión 2 — API musical y búsqueda](#sesión-2--api-musical-y-búsqueda)
  - [Sesión 3 — Reproductor musical](#sesión-3--reproductor-musical)
  - [Sesión 4 — Biblioteca y persistencia](#sesión-4--biblioteca-y-persistencia)
- [Versiones](#versiones)
- [Flujo Git](#flujo-git)
- [Convención de commits](#convención-de-commits)
- [Recursos](#recursos)
- [Cómo iniciar](#cómo-iniciar)
- [Criterios generales de calidad](#criterios-generales-de-calidad)

---

## Objetivo del proyecto

Construir una aplicación web musical utilizando únicamente tecnologías del navegador y APIs públicas gratuitas.

Al finalizar, BeatFlow deberá permitir:

- visualizar canciones destacadas;
- consultar tendencias;
- buscar música;
- mostrar artistas y portadas;
- seleccionar canciones;
- reproducir audio;
- pausar y continuar;
- controlar progreso;
- controlar volumen;
- avanzar y regresar canciones;
- mantener una cola de reproducción;
- guardar favoritos;
- mostrar canciones escuchadas recientemente;
- persistir preferencias con LocalStorage;
- funcionar correctamente en desktop, tablet y móvil.

[⬆ Regresar al índice](#índice)

---

## Stack tecnológico

| Tecnología | Uso |
|---|---|
| HTML5 | Estructura semántica |
| TailwindCSS 4 | UI responsive |
| CSS | Design Tokens y estilos globales |
| JavaScript ES6+ | Lógica |
| ES Modules | Modularización |
| Fetch / SDK | Consumo de API |
| Audius API | Música, artistas, búsquedas y streaming |
| HTML Audio API | Reproducción |
| LocalStorage | Persistencia |
| Git | Control de versiones |
| GitHub | Repositorio |

[⬆ Regresar al índice](#índice)

---

## Restricciones del proyecto

Este proyecto no utilizará:

- React
- Vue
- Angular
- Nuxt
- Node.js backend
- Express
- Firebase
- Base de datos propia

El objetivo es comprender primero:

```text
HTML
+
CSS
+
JavaScript
+
DOM
+
HTTP
+
APIs
+
Estado
+
Persistencia
```

[⬆ Regresar al índice](#índice)

---

## Estructura general

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
│   ├── data/
│   │   └── mock.data.js
│   ├── api/
│   │   └── audius.api.js
│   ├── services/
│   │   ├── player.service.js
│   │   └── storage.service.js
│   └── ui/
│       ├── home.ui.js
│       ├── search.ui.js
│       ├── library.ui.js
│       └── player.ui.js
│
└── docs/
    ├── README.md
    ├── sesion-01/
    │   └── README.md
    ├── sesion-02/
    │   └── README.md
    ├── sesion-03/
    │   └── README.md
    └── sesion-04/
        └── README.md
```

[⬆ Regresar al índice](#índice)

---

## Arquitectura conceptual

```text
                  USUARIO
                     │
                     ▼
               HTML / DOM
                     │
                     ▼
                  app.js
                     │
          ┌──────────┼──────────┐
          │          │          │
          ▼          ▼          ▼
        UI        Services     State
          │          │
          │          ├───────────────┐
          │          │               │
          ▼          ▼               ▼
         DOM    Audius API      LocalStorage
                     │
                     ▼
              HTML Audio API
```

[⬆ Regresar al índice](#índice)

---

## Roadmap

```text
Sesión 1
   │
   ▼
UI + Responsive + Mock Data
   │
   ▼
v0.1.0
   │
   ▼
Sesión 2
   │
   ▼
Audius API + Search
   │
   ▼
v0.2.0
   │
   ▼
Sesión 3
   │
   ▼
Audio Player + Queue
   │
   ▼
v0.3.0
   │
   ▼
Sesión 4
   │
   ▼
Favorites + History + LocalStorage
   │
   ▼
v1.0.0
```

[⬆ Regresar al índice](#índice)

---

## Sesiones

### Sesión 1 — UI/UX y estructura

**Objetivo:** construir la primera versión visual y responsive de BeatFlow.

**Versión:** `v0.1.0`

Incluye:

- sidebar desktop;
- header;
- buscador visual;
- hero;
- cards dinámicas;
- canciones destacadas;
- escuchados recientemente;
- player visual;
- navegación móvil;
- datos mock.

[📘 Abrir Sesión 1](./docs/sesion-01/README.md)

---

### Sesión 2 — API musical y búsqueda

**Objetivo:** reemplazar progresivamente datos mock por información real.

**Versión:** `v0.2.0`

Incluye:

- REST API;
- Audius;
- Fetch;
- async/await;
- búsqueda;
- tendencias;
- loading;
- empty state;
- error state.

[📘 Abrir Sesión 2](./docs/sesion-02/README.md)

---

### Sesión 3 — Reproductor musical

**Objetivo:** agregar reproducción de audio real.

**Versión:** `v0.3.0`

Incluye:

- play;
- pause;
- progress;
- duration;
- volume;
- queue;
- previous;
- next.

[📘 Abrir Sesión 3](./docs/sesion-03/README.md)

---

### Sesión 4 — Biblioteca y persistencia

**Objetivo:** completar BeatFlow con persistencia local.

**Versión:** `v1.0.0`

Incluye:

- favoritos;
- historial;
- biblioteca;
- preferencias;
- LocalStorage;
- accesibilidad;
- responsive final.

[📘 Abrir Sesión 4](./docs/sesion-04/README.md)

[⬆ Regresar al índice](#índice)

---

## Versiones

| Versión | Sesión | Alcance |
|---|---:|---|
| `v0.1.0` | 1 | UI responsive y datos mock |
| `v0.2.0` | 2 | API y búsqueda |
| `v0.3.0` | 3 | Reproductor |
| `v1.0.0` | 4 | Biblioteca y persistencia |

[⬆ Regresar al índice](#índice)

---

## Flujo Git

```text
main
 │
 ├── feature/session-01-ui
 ├── feature/session-02-api
 ├── feature/session-03-player
 └── feature/session-04-library
```

Ejemplo:

```bash
git checkout -b feature/session-01-ui
```

Al terminar:

```bash
git checkout main
git merge feature/session-01-ui
```

Crear tag:

```bash
git tag -a v0.1.0 -m "BeatFlow session 1"
```

[⬆ Regresar al índice](#índice)

---

## Convención de commits

```text
chore: create project structure
feat: add responsive sidebar
style: add BeatFlow theme
feat: render trending tracks
feat: integrate Audius API
feat: implement music search
feat: implement audio player
feat: add favorite tracks
fix: improve mobile player
docs: update session instructions
```

[⬆ Regresar al índice](#índice)

---

## Recursos

### TailwindCSS

https://tailwindcss.com/

Play CDN:

```html
<script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
```

Documentación:

https://tailwindcss.com/docs/installation/play-cdn

### Audius

https://audius.co/

Documentación:

https://docs.audius.co/

### MDN Web Docs

https://developer.mozilla.org/

[⬆ Regresar al índice](#índice)

---

## Cómo iniciar

### 1. Clonar repositorio

```bash
git clone URL_DEL_REPOSITORIO
```

### 2. Entrar al proyecto

```bash
cd aplicaciones-de-internet/projects/beatflow
```

### 3. Abrir VS Code

```bash
code .
```

### 4. Consultar documentación

[📚 Abrir índice de documentación](./docs/README.md)

[⬆ Regresar al índice](#índice)

---

## Criterios generales de calidad

Cada versión debe cumplir:

- HTML semántico;
- interfaz responsive;
- JavaScript modular;
- sin errores de consola;
- estados visuales claros;
- navegación accesible;
- imágenes con `alt`;
- focus visible;
- commits pequeños;
- nombres descriptivos;
- sin secretos en el repositorio.

---

## Inicio del proyecto

[▶ Comenzar con la Sesión 1](./docs/sesion-01/README.md)

[⬆ Regresar al índice](#índice)
