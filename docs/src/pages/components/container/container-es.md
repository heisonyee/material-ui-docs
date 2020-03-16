---
title: Container React component
components: Container
---

# Container

<p class="description">El container centra el contenido horizontalmente. Es el elemento más básico del layout.</p>

Si bien los contenedores pueden anidarse, la mayoria de los layouts no requieren un contenedor anidado. 

## Fluido

El ancho de un container está limitado por el valor de la propiedad `maxWidth`.

{{"demo": "pages/components/container/SimpleContainer.js", "iframe": true, "defaultCodeOpen": false}}

```jsx
<Container maxWidth="sm">
```

## Fijo

If you prefer to design for a fixed set of sizes instead of trying to accommodate a fully fluid viewport, you can set the `fixed` property. The max-width matches the min-width of the current breakpoint.

{{"demo": "pages/components/container/FixedContainer.js", "iframe": true, "defaultCodeOpen": false}}

```jsx
<Container fixed>
```