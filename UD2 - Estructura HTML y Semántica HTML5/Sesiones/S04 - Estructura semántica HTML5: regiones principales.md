---
asignatura: DIW
unidad: UD2
sesion: 04
tipo: material-alumnado
estado: preparado
programacion: "UP2 - Estructura HTML y Semántica HTML5"
duracion: "55 minutos"
---

# Sesión 04 · Estructura semántica HTML5: regiones principales

> [!abstract] Propósito de la sesión
> Organizar una página mediante elementos semánticos que describen la función de cada región.

## Objetivos de aprendizaje
- Explicar qué aporta la semántica HTML.
- Identificar las regiones habituales de una página.
- Utilizar `header`, `nav`, `main` y `footer` con sentido.

## Desarrollo de contenidos

## 1. De contenedores genéricos a estructura semántica

Un documento puede contener muchos elementos, pero no todos describen lo mismo. La semántica permite expresar qué función cumple cada parte: cabecera, navegación, contenido principal o pie.

La estructura semántica ayuda a las personas que leen el código, a los navegadores y a las tecnologías de asistencia. No garantiza por sí sola que una web sea accesible, pero proporciona una base más comprensible.

## 2. Elementos estructurales principales

- `<header>`: cabecera de una página o de una sección. Puede contener título, logotipo o información introductoria.
- `<nav>`: bloque de navegación con enlaces o mecanismos para desplazarse por el sitio o por una parte de él.
- `<main>`: contenido principal del documento. Habitualmente hay un único `<main>` visible por página.
- `<footer>`: pie de una página o de una sección. Puede contener autoría, contacto o información relacionada.

## 3. Ejemplo de estructura global

```html
<body>
    <header>
        <h1>Centro de formación</h1>
    </header>

    <nav aria-label="Navegación principal">
        <!-- Enlaces de navegación -->
    </nav>

    <main>
        <h2>Oferta formativa</h2>
        <p>Consulta nuestros ciclos.</p>
    </main>

    <footer>
        <p>Centro de formación · Curso 2026-2027</p>
    </footer>
</body>
```

`aria-label` es un atributo de accesibilidad que permite dar un nombre a la región de navegación. En esta unidad se introduce como ejemplo de etiquetado descriptivo, sin desarrollar todavía el bloque específico de accesibilidad.

## 4. Semántica frente a apariencia

`<header>` no significa “barra azul superior”, ni `<footer>` significa “caja situada abajo”. Son elementos que expresan función. La posición, los colores y la distribución se controlan mediante CSS.

## 5. ¿Puede haber varios `header` o `footer`?

Sí. Pueden aparecer en el documento y también dentro de elementos que representan contenido independiente o secciones. Su significado depende del contexto. No debemos introducirlos de forma automática en cualquier contenedor.

## 6. Errores frecuentes

- Utilizar `<nav>` para cualquier grupo de enlaces, aunque no sea navegación relevante.
- Colocar todo el documento dentro de `<main>` sin distinguir cabeceras y pies globales.
- Utilizar etiquetas semánticas solo porque “suenan modernas”.
- Pensar que la semántica determina el aspecto visual.

## Ejemplo guiado

### Ejemplo guiado: página de un centro

Dibuja primero cuatro regiones: cabecera, navegación, contenido principal y pie. Después traduce cada región a su elemento HTML correspondiente. Comprueba que el contenido principal está dentro de `main` y que el menú está dentro de `nav`.

## Actividades prácticas

### E13 · Mapa semántico

Sobre tres capturas de páginas distintas, señala qué zonas podrían ser `header`, `nav`, `main` y `footer`. Justifica los casos dudosos.

### E14 · Convertir estructura genérica

Recibe un documento construido solo con `div`. Sustituye los contenedores cuyo propósito esté claro por elementos semánticos adecuados.

### E15 · Página institucional

Crea la estructura semántica de la página principal de un centro educativo con cabecera, navegación, contenido principal y pie.

### E16 · Detectar usos incorrectos

Analiza un documento donde se usan tres `main`, varios `nav` sin función clara y `footer` como sustituto de un párrafo. Propón una estructura mejor.

## Reto de aplicación

Diseña la estructura HTML de un portal de noticias del centro. Incluye cabecera global, navegación principal, contenido principal y pie. Todavía no añadas artículos individuales.

## Errores que debes evitar

- Elegir etiquetas por su apariencia en lugar de por su significado.
- Escribir código sin revisar el anidamiento.
- Olvidar las etiquetas asociadas a los controles de formulario.
- Dar por válido un documento solo porque el navegador lo muestra.

## Resumen de la sesión

Al finalizar debes poder explicar los conceptos principales, construir un ejemplo pequeño y justificar las decisiones de marcado realizadas.

## Autoevaluación

- [ ] Sé explicar qué significa semántica en HTML.
- [ ] Diferencio cabecera, navegación, contenido principal y pie.
- [ ] No confundo función con apariencia.
- [ ] Sé cuándo tiene sentido utilizar `nav`.

## Registro personal

- Dudas que me quedan:
- Errores que he corregido:
- Qué necesito practicar de nuevo:
