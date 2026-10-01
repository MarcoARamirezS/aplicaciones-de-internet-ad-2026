# Aplicaciones de Internet — Proyectos

Repositorio académico de proyectos prácticos desarrollados para la materia **Aplicaciones de Internet**.

Cada proyecto se desarrolla de forma evolutiva e incluye:

- planeación;
- documentación;
- código;
- prácticas;
- control de versiones;
- validaciones;
- versiones incrementales.

---

## Índice de proyectos

| # | Proyecto | Tecnologías | Sesiones | Acceso |
|---:|---|---|---:|---|
| 01 | BeatFlow | HTML5, TailwindCSS, CSS, JavaScript, APIs | 4 | [Abrir proyecto](./projects/betflow/README.md) |
| 02 | UniDash 360 | HTML5, TailwindCSS, JavaScript, LocalStorage, Chart.js, APIs | 3 | [Abrir proyecto](./projects/unidash360/README.md) |

---

## Estructura general del repositorio

```text
aplicaciones-de-internet-ad-2026/
│
├── README.md
│
└── projects/
    │
    ├── beatflow/
    │   ├── README.md
    │   └── docs/
    │       ├── README.md
    │       ├── sesion-01/
    │       ├── sesion-02/
    │       ├── sesion-03/
    │       └── sesion-04/
    │
    ├── unidash360/
    │   ├── README.md
    │   └── docs/
    │       ├── README.md
    │       ├── sesion-01/
    │       ├── sesion-02/
    │       └── sesion-03/
    │
    └── futuros-proyectos/
```

---

## Cómo utilizar este repositorio

1. Seleccionar un proyecto desde el índice.
2. Abrir el `README.md` del proyecto.
3. Consultar el índice de sesiones.
4. Iniciar con la sesión correspondiente.
5. Seguir los documentos en el orden indicado.
6. Realizar los commits solicitados.
7. Ejecutar la validación de cada sesión.
8. Crear el tag correspondiente cuando la versión esté terminada.

---

## Proyectos

### 01 — BeatFlow

Aplicación web musical inspirada en plataformas modernas de streaming.

Se utiliza como proyecto evolutivo para practicar:

- HTML5;
- TailwindCSS;
- CSS;
- JavaScript;
- ES Modules;
- DOM;
- APIs REST;
- JSON;
- Fetch;
- HTML Audio API;
- LocalStorage;
- Git;
- GitHub.

**Duración:** 4 sesiones de 1 hora con 30 minutos.

[▶ Abrir BeatFlow](./projects/betflow/README.md)

---


### 02 — UniDash 360

Dashboard personal universitario construido con una estrategia **UI-first**: primero se desarrolla toda la experiencia visual con datos mock; después se conectan estado y persistencia local; finalmente se integran endpoints públicos.

Se utiliza para practicar:

- diseño responsive y componentes UI;
- datos mock y renderizado dinámico;
- formularios y CRUD;
- LocalStorage;
- transformación de datos con `filter`, `map` y `reduce`;
- Chart.js;
- Geolocation API;
- Fetch y APIs REST;
- clima, divisas y noticias;
- manejo de estados `loading`, `error` y fallback;
- Git y versionado incremental.

**Duración:** 3 sesiones de 1 hora con 30 minutos.

[▶ Abrir UniDash 360](./projects/unidash360/README.md)

---

## Convención para nuevos proyectos

Todos los proyectos deben colocarse dentro de:

```text
projects/
```

Ejemplo:

```text
projects/
├── beatflow/
├── proyecto-02/
├── proyecto-03/
└── proyecto-04/
```

Cada proyecto debe incluir su propio:

```text
README.md
```

El `README.md` principal del repositorio funcionará únicamente como **índice general de proyectos**.
