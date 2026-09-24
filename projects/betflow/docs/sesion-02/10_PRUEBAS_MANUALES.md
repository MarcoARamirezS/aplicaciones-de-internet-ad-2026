# BeatFlow — Pruebas manuales Sesión 2

[📘 Sesión 2](./README.md) · [⬅ Documentación](../README.md) · [🏠 BeatFlow](../../README.md) · [📚 Índice general](../../../../README.md) · [◀ Anterior](./09_APP_JS.md) · [Siguiente ▶](./12_VALIDACION_SESION_2.md)

---

## 1. SDK

```javascript
window.audiusSdk
```

Debe existir.

## 2. Home

```text
Loading → Trending real
```

## 3. API Key inválida

Esperado:

```text
Error State + Reintentar
```

## 4. Search

Buscar:

```text
electronic
```

Esperado:

```text
Loading → Resultados
```

## 5. Query corta

```text
a
```

Debe mostrar instrucción/Empty State.

## 6. Selección

Seleccionar una canción debe actualizar visualmente:

```text
title
artist
cover
```

## 7. Network

Revisar solicitudes al cargar Home y ejecutar Search.

## 8. Responsive

```text
375px
768px
1024px
1440px
```

## 9. Console

```text
0 errores no controlados
```

---

## Navegación

[📘 Sesión 2](./README.md) · [⬅ Documentación](../README.md) · [🏠 BeatFlow](../../README.md) · [📚 Índice general](../../../../README.md) · [◀ Anterior](./09_APP_JS.md) · [Siguiente ▶](./12_VALIDACION_SESION_2.md)
