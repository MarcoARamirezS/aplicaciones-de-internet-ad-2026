# UniDash 360

Dashboard personal universitario desarrollado como proyecto evolutivo para la materia **Aplicaciones de Internet**.

UniDash 360 combina información creada por el usuario con información obtenida de servicios públicos de Internet. El objetivo es que el estudiante construya una aplicación que se sienta cercana a un producto real y no únicamente a un ejercicio aislado de `fetch()`.

[📚 Índice general](../../README.md)

---

## Índice

- [Objetivo](#objetivo)
- [Resultado final](#resultado-final)
- [Stack tecnológico](#stack-tecnológico)
- [Restricciones](#restricciones)
- [Arquitectura](#arquitectura)
- [Modelo de datos](#modelo-de-datos)
- [APIs externas](#apis-externas)
- [Sesiones](#sesiones)
- [Versiones](#versiones)
- [Documentación](#documentación)
- [Flujo Git](#flujo-git)
- [Ejecución](#ejecución)
- [Código de referencia](#código-de-referencia)

---

## Objetivo

Construir un **dashboard personal universitario** capaz de concentrar productividad, finanzas e información contextual.

Al finalizar el proyecto permitirá:

- crear, editar, completar, reabrir, filtrar y eliminar tareas;
- guardar las tareas en `LocalStorage`;
- registrar ingresos y egresos;
- clasificar movimientos financieros;
- calcular balance y tasa de ahorro;
- generar gráficas a partir de datos propios;
- detectar la ubicación del navegador con autorización del usuario;
- identificar ciudad, región y país;
- mostrar el clima de la ubicación;
- seleccionar una moneda base de acuerdo con el país;
- consultar tipos de cambio internacionales;
- consultar un histórico aproximado de 30 días;
- convertir cantidades entre monedas;
- consultar noticias recientes por país y localidad;
- trabajar con estados de carga, error y ausencia de datos;
- funcionar en desktop, tablet y móvil.

[⬆ Regresar al índice](#índice)

---

## Resultado final

```text
UniDash 360
│
├── Dashboard
│   ├── Balance
│   ├── Ingresos
│   ├── Egresos
│   ├── Tareas pendientes
│   ├── Clima
│   ├── Tipos de cambio
│   └── Noticias
│
├── Tareas
│   ├── Crear
│   ├── Editar
│   ├── Completar / reabrir
│   ├── Eliminar
│   └── Filtrar
│
├── Finanzas
│   ├── Ingresos
│   ├── Egresos
│   ├── Categorías
│   └── Historial
│
├── Estadísticas
│   ├── Ingresos vs egresos
│   ├── Gastos por categoría
│   └── Estado de tareas
│
├── Divisas
│   ├── Tasas actuales
│   ├── Histórico
│   └── Conversor
│
└── Noticias
    ├── General
    ├── Tecnología
    ├── Negocios
    ├── Ciencia
    ├── Deportes
    ├── Entretenimiento
    └── Salud
```

[⬆ Regresar al índice](#índice)

---

## Stack tecnológico

| Tecnología | Uso |
|---|---|
| HTML5 | Estructura semántica |
| TailwindCSS 4 | Utilidades de UI |
| CSS | Design tokens y estilos del dashboard |
| JavaScript ES6+ | Lógica de aplicación |
| ES Modules | Organización por módulos |
| DOM | Renderizado e interacción |
| LocalStorage | Persistencia local |
| Chart.js | Visualización de datos |
| Fetch API | Consumo HTTP |
| Browser Geolocation API | Coordenadas del dispositivo |
| BigDataCloud | Reverse geocoding |
| Open-Meteo | Clima |
| Frankfurter v2 | Tipos de cambio e histórico |
| GNews | Noticias |
| Git | Control de versiones |
| GitHub | Repositorio |

[⬆ Regresar al índice](#índice)

---

## Restricciones

Durante este proyecto **no se utilizarán**:

- React;
- Vue;
- Angular;
- Nuxt;
- backend propio;
- Express;
- Firebase;
- base de datos remota.

La intención académica es dominar primero:

```text
HTML
+
CSS
+
JavaScript
+
DOM
+
CRUD
+
LocalStorage
+
HTTP
+
REST
+
JSON
+
Fetch
+
async/await
+
APIs externas
+
Visualización de datos
```

[⬆ Regresar al índice](#índice)

---

## Arquitectura

```text
                            USUARIO
                               │
                               ▼
                         HTML / DOM
                               │
                               ▼
                            app.js
                               │
                ┌──────────────┼──────────────┐
                │              │              │
                ▼              ▼              ▼
             Modules        Services       Chart.js
                │              │
                │        ┌─────┴─────────────────────────┐
                │        │                               │
                ▼        ▼                               ▼
          LocalStorage  Browser APIs               APIs externas
                │        │                               │
        ┌───────┴─────┐  │        ┌──────────┬──────────┼─────────┐
        ▼             ▼  ▼        ▼          ▼          ▼         ▼
      Tasks       Transactions Location  BigDataCloud Open-Meteo Frankfurter
                                                            │
                                                            ▼
                                                           GNews
```

La aplicación combina tres clases de información:

```text
DATOS DEL USUARIO
tareas + movimientos + preferencias
            │
            ▼
       LocalStorage

DATOS EXTERNOS
clima + divisas + noticias
            │
            ▼
          APIs

DATOS DERIVADOS
balance + ahorro + métricas + gráficas
            │
            ▼
        JavaScript
```

[⬆ Regresar al índice](#índice)

---

## Modelo de datos

### Tarea

```javascript
{
  id: "uuid",
  title: "Entregar proyecto",
  description: "Subir repositorio",
  category: "Universidad",
  priority: "high",
  status: "pending",
  dueDate: "2026-10-02",
  createdAt: "..."
}
```

### Movimiento financiero

```javascript
{
  id: "uuid",
  description: "Beca",
  type: "income",
  amount: 4500,
  category: "Beca",
  date: "2026-09-28"
}
```

### Preferencias

```javascript
{
  baseCurrency: "MXN",
  newsCategory: "general",
  location: null
}
```

[⬆ Regresar al índice](#índice)

---

## APIs externas

| Servicio | Uso | API key |
|---|---|---|
| Browser Geolocation API | Obtener coordenadas con permiso | No |
| BigDataCloud | Convertir coordenadas a localidad | No |
| Open-Meteo | Clima actual | No |
| Frankfurter v2 | Divisas e histórico | No |
| GNews | Noticias | Sí |

La API key de GNews se utiliza únicamente con fines académicos en `localhost`. El archivo local que contiene la key se excluye de Git, pero una key usada directamente desde frontend **sigue siendo visible desde el navegador**. En producción debe utilizarse un backend o función server-side.

[⬆ Regresar al índice](#índice)

---

## Sesiones

### Sesión 1 — Dashboard, tareas y LocalStorage

**Versión:** `v0.1.0`

Objetivo:

Construir la base visual y el primer módulo persistente.

Incluye:

- estructura del proyecto;
- sidebar;
- navegación entre vistas;
- dashboard de productividad;
- CRUD de tareas;
- filtros;
- tareas vencidas;
- `LocalStorage`;
- responsive design.

[📘 Abrir Sesión 1](./docs/sesion-01/README.md)

---

### Sesión 2 — Finanzas, métricas y Chart.js

**Versión:** `v0.2.0`

Objetivo:

Agregar información financiera propia y transformarla en métricas y gráficas.

Incluye:

- ingresos;
- egresos;
- categorías;
- historial;
- balance;
- tasa de ahorro;
- `filter()`;
- `reduce()`;
- Chart.js;
- estadísticas de tareas y finanzas.

[📘 Abrir Sesión 2](./docs/sesion-02/README.md)

---

### Sesión 3 — Ubicación, clima, divisas y noticias

**Versión:** `v1.0.0`

Objetivo:

Conectar el dashboard con servicios reales de Internet.

Incluye:

- Browser Geolocation API;
- BigDataCloud;
- Open-Meteo;
- moneda base;
- Frankfurter;
- histórico de divisas;
- conversor;
- GNews;
- integración final;
- estados de error.

[📘 Abrir Sesión 3](./docs/sesion-03/README.md)

[⬆ Regresar al índice](#índice)

---

## Versiones

| Versión | Sesión | Resultado |
|---|---:|---|
| `v0.1.0` | 1 | Dashboard + Tareas + LocalStorage |
| `v0.2.0` | 2 | Finanzas + Estadísticas + Chart.js |
| `v1.0.0` | 3 | APIs externas + Dashboard final |

[⬆ Regresar al índice](#índice)

---

## Documentación

[📚 Abrir documentación completa](./docs/README.md)

Cada sesión contiene:

- planeación;
- recursos;
- estructura;
- código completo de cada archivo creado o modificado;
- pasos de clase;
- pruebas manuales;
- validación;
- comandos Git.

[⬆ Regresar al índice](#índice)

---

## Flujo Git

Ramas sugeridas:

```text
main
├── feature/session-01-tasks
├── feature/session-02-finance-charts
└── feature/session-03-external-apis
```

Tags:

```text
v0.1.0
v0.2.0
v1.0.0
```

[⬆ Regresar al índice](#índice)

---

## Ejecución

Se recomienda:

```text
Visual Studio Code
+
Live Server
```

No se requiere Node.js ni npm.

No abras el proyecto mediante:

```text
file://
```

Se utiliza `localhost` porque los ES Modules, la geolocalización y la integración de GNews funcionan correctamente en un contexto de desarrollo HTTP local.

[⬆ Regresar al índice](#índice)

---

## Código de referencia

La documentación contiene el código completo de cada archivo que se crea o modifica.

El profesor dispone además de un paquete separado con snapshots ejecutables al cierre de:

```text
v0.1.0
v0.2.0
v1.0.0
```

---

[📚 Índice general](../../README.md) · [📘 Abrir documentación](./docs/README.md)
