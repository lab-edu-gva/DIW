---
asignatura: DIW
unidad: UD2
sesion: 02
tipo: material-alumnado
estado: preparado
programacion: "UP2 - Estructura HTML y Semántica HTML5"
duracion: "55 minutos"
---

# Sesión 02 · Sintaxis HTML, anidamiento, comentarios y contenido textual

> [!abstract] Propósito de la sesión
> Escribir documentos HTML legibles, bien anidados y con una jerarquía textual coherente.

## Objetivos de aprendizaje
- Aplicar correctamente etiquetas de apertura y cierre.
- Anidar elementos respetando la estructura del documento.
- Utilizar comentarios y elementos básicos de texto.

## Desarrollo de contenidos

## 1. Reglas básicas de escritura

HTML no exige que escribamos cada etiqueta en una línea, pero una buena indentación facilita leer y mantener el documento. Es recomendable utilizar minúsculas en los nombres de etiquetas y atributos, comillas dobles para los valores y una sangría coherente.

```html
<body>
    <h1>Noticias del centro</h1>
    <p>Últimas novedades del curso.</p>
</body>
```

## 2. Anidamiento

Anidar significa colocar un elemento dentro de otro. Los elementos deben cerrarse en orden inverso al que se abrieron. Es la regla de la pila: el último que entra es el primero que sale.

Correcto:

```html
<p>Consulta la <strong>documentación oficial</strong>.</p>
```

Incorrecto:

```html
<p>Consulta la <strong>documentación oficial.</p></strong>
```

El segundo ejemplo mezcla los cierres y produce una estructura incorrecta o ambigua.

## 3. Encabezados y párrafos

Los encabezados se escriben con `<h1>` a `<h6>`. Expresan niveles de títulos y subtítulos, no tamaños visuales. Normalmente una página debe tener un título principal claro y después organizar sus apartados de forma jerárquica.

```html
<h1>Guía de HTML</h1>
<h2>Estructura del documento</h2>
<p>Todo documento HTML tiene una estructura básica.</p>
<h2>Elementos de texto</h2>
<h3>Énfasis</h3>
<p>Podemos destacar <strong>información importante</strong>.</p>
```

`<p>` representa un párrafo. No debe utilizarse para crear espacios en blanco ni para simular márgenes.

## 4. Énfasis y significado

- `<strong>` indica importancia o relevancia.
- `<em>` expresa énfasis que puede cambiar el sentido de una frase.
- `<br>` introduce un salto de línea dentro del mismo contenido, pero no debe utilizarse para separar párrafos.
- `<hr>` representa una separación temática entre bloques de contenido.

No elijas una etiqueta únicamente por cómo aparece visualmente. El significado debe ser correcto; la apariencia se tratará con CSS.

## 5. Comentarios HTML

Los comentarios permiten dejar anotaciones en el código fuente. El navegador no los presenta como contenido normal:

```html
<!-- Este es el título principal de la página -->
<h1>Catálogo de cursos</h1>
```

No deben utilizarse para guardar contraseñas ni información privada: el código fuente puede consultarse desde el navegador.

## 6. Listas

Aunque el foco es la sintaxis, las listas son útiles para practicar anidamiento:

```html
<ul>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
</ul>
```

`<ul>` crea una lista no ordenada, `<ol>` una lista ordenada y `<li>` cada elemento de la lista.

## Ejemplo guiado

### Ejemplo guiado: índice de una guía

Construye un documento con un `<h1>`, dos `<h2>`, al menos un `<h3>`, párrafos, una lista y un comentario. Indenta cada nivel. Comprueba que todos los elementos se cierran correctamente.

## Actividades prácticas

### E05 · Reparar anidamiento

Corrige cinco fragmentos con cierres desordenados. En cada caso, marca qué etiqueta se abrió primero y cuál debe cerrarse primero.

### E06 · Jerarquía de títulos

Transforma un texto desordenado sobre una biblioteca en una estructura con un único título principal, apartados y subapartados coherentes.

### E07 · Semántica textual

Decide cuándo usarías `strong`, `em`, `br` y `hr`. Escribe un ejemplo correcto de cada uno y explica por qué no son intercambiables.

### E08 · Documento comentado

Crea `guia-html.html` con dos apartados, una lista de cinco elementos y tres comentarios útiles. Aplica indentación consistente.

## Reto de aplicación

Elabora una pequeña guía de normas del aula con encabezados jerárquicos, párrafos, una lista ordenada de pasos y una lista no ordenada de materiales. El código debe quedar correctamente anidado.

## Errores que debes evitar

- Elegir etiquetas por su apariencia en lugar de por su significado.
- Escribir código sin revisar el anidamiento.
- Olvidar las etiquetas asociadas a los controles de formulario.
- Dar por válido un documento solo porque el navegador lo muestra.

## Resumen de la sesión

Al finalizar debes poder explicar los conceptos principales, construir un ejemplo pequeño y justificar las decisiones de marcado realizadas.

## Autoevaluación

- [ ] Cierro los elementos en el orden correcto.
- [ ] Utilizo encabezados por jerarquía y no por tamaño.
- [ ] Distingo párrafo, salto de línea y separación temática.
- [ ] Sé añadir comentarios sin confundirlos con contenido visible.

## Registro personal

- Dudas que me quedan:
- Errores que he corregido:
- Qué necesito practicar de nuevo:
