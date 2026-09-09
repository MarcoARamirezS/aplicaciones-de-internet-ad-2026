# BeatFlow

Aplicación web musical desarrollada como proyecto evolutivo para la materia **Aplicaciones de Internet**.

BeatFlow está inspirado en la experiencia de plataformas modernas de streaming musical, pero utiliza una identidad visual propia y un stack deliberadamente simple para reforzar fundamentos de desarrollo frontend.


---

# Objetivo del proyecto

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

---

# Stack tecnológico

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

---

# Restricciones del proyecto

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

---

# Estructura general

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
│   ├── api/
│   │   └── audius.api.js
│   │
│   ├── services/
│   │   ├── player.service.js
│   │   └── storage.service.js
│   │
│   └── ui/
│       ├── home.ui.js
│       ├── search.ui.js
│       ├── library.ui.js
│       └── player.ui.js
│
└── docs/
    ├── README.md
    │
    ├── sesion-01/
    │   └── README.md
    │
    ├── sesion-02/
    │   └── README.md
    │
    ├── sesion-03/
    │   └── README.md
    │
    └── sesion-04/
        └── README.md
```

---

# Arquitectura conceptual

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

---

# Roadmap

BeatFlow se desarrolla en cuatro sesiones.

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

---

# Sesión 1 — UI/UX y estructura

## Objetivo

Construir la primera versión visual y responsive de BeatFlow.

## Temas

- HTML5
- TailwindCSS
- CSS
- Responsive Design
- Design Tokens
- JavaScript ES Modules
- DOM
- Arrays
- `map()`
- `find()`
- Event Delegation
- Estado básico
- Git

## Resultado esperado

```text
v0.1.0
```

Incluye:

- sidebar desktop;
- header;
- buscador visual;
- hero;
- canciones destacadas;
- cards dinámicas;
- escuchados recientemente;
- player visual;
- navegación móvil;
- responsive design;
- datos mock.

## Documentación

[Ir a la Sesión 1](./docs/sesion-01/README.md)

---

# Sesión 2 — API musical y búsqueda

## Objetivo

Reemplazar progresivamente los datos simulados por información proveniente de una API pública gratuita.

## Temas

- REST API
- HTTP
- JSON
- Fetch
- async / await
- Promises
- try / catch
- API musical
- búsqueda
- estados Loading / Empty / Error
- transformación de datos

## Resultado esperado

```text
v0.2.0
```

Incluye:

- conexión con Audius;
- canciones reales;
- artistas reales;
- portadas reales;
- búsqueda;
- tendencias;
- manejo de errores.

## Documentación

[Ir a la Sesión 2](./docs/sesion-02/README.md)

---

# Sesión 3 — Reproductor musical

## Objetivo

Agregar reproducción real de audio y comportamiento completo del player.

## Temas

- HTMLAudioElement
- Audio API
- play
- pause
- currentTime
- duration
- volume
- progress
- ended
- queue
- previous
- next

## Resultado esperado

```text
v0.3.0
```

Incluye:

- reproducción;
- pausa;
- progreso;
- duración;
- volumen;
- canción anterior;
- canción siguiente;
- cola de reproducción.

## Documentación

[Ir a la Sesión 3](./docs/sesion-03/README.md)

---

# Sesión 4 — Biblioteca y persistencia

## Objetivo

Convertir BeatFlow en una aplicación persistente.

## Temas

- LocalStorage
- serialización JSON
- favoritos
- historial
- preferencias
- persistencia
- UX
- accesibilidad
- responsive final

## Resultado esperado

```text
v1.0.0
```

Incluye:

- favoritos;
- escuchados recientemente;
- biblioteca;
- preferencias;
- persistencia;
- estados vacíos;
- accesibilidad;
- revisión final responsive.

## Documentación

[Ir a la Sesión 4](./docs/sesion-04/README.md)

---

# Versiones

| Versión | Sesión | Alcance |
|---|---:|---|
| `v0.1.0` | 1 | UI responsive y datos mock |
| `v0.2.0` | 2 | API y búsqueda |
| `v0.3.0` | 3 | Reproductor |
| `v1.0.0` | 4 | Biblioteca y persistencia |

---

# Flujo Git

Se utilizará un flujo simplificado inspirado en GitFlow.

```text
main
 │
 ├── feature/session-01-ui
 │
 ├── feature/session-02-api
 │
 ├── feature/session-03-player
 │
 └── feature/session-04-library
```

Crear una rama:

```bash
git checkout -b feature/session-01-ui
```

Trabajar y hacer commits:

```bash
git add .
git commit -m "feat: create BeatFlow base layout"
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

---

# Convención de commits

Ejemplos:

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

---

# Recursos

## TailwindCSS

```text
https://tailwindcss.com/
```

Play CDN:

```html
<script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
```

Documentación:

```text
https://tailwindcss.com/docs/installation/play-cdn
```

---

## Audius

```text
https://audius.co/
```

Documentación:

```text
https://docs.audius.co/
```

---

## MDN Web Docs

```text
https://developer.mozilla.org/
```

---

# Cómo iniciar

## 1. Clonar repositorio

```bash
git clone URL_DEL_REPOSITORIO
```

## 2. Entrar al proyecto

```bash
cd aplicaciones-de-internet/projects/beatflow
```

## 3. Abrir VS Code

```bash
code .
```

## 4. Consultar la primera sesión

Abrir:

```text
docs/sesion-01/README.md
```

o desde GitHub:

[Comenzar con la Sesión 1](./docs/sesion-01/README.md)

---

# Cómo ejecutar

Durante las primeras sesiones se recomienda utilizar **VS Code + Live Server**.

Abrir:

```text
index.html
```

y seleccionar:

```text
Open with Live Server
```

---

# Criterios generales de calidad

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

# Final esperado

Al finalizar:

```text
BeatFlow v1.0.0

HTML5
+
TailwindCSS
+
CSS
+
JavaScript
+
REST API
+
Audio
+
LocalStorage
+
Responsive Design
+
Git
```

---

# Inicio del proyecto

La implementación comienza en:

[Sesión 1 — UI/UX y estructura](./docs/sesion-01/README.md)
