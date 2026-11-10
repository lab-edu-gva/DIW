---
asignatura: DIW
unidad: UD2
sesion: 01
tipo: material-alumnado
estado: preparado
programacion: "UP2 - Estructura HTML y Semántica HTML5"
duracion: "55 minutos"
---

# Sesión 01 · HTML y estructura básica de un documento web

> [!abstract] Propósito de la sesión
> Comprender qué es HTML, qué papel desempeña en una página web y cómo se organiza un documento HTML5 mínimo.

## Objetivos de aprendizaje
- Distinguir contenido, estructura y presentación.
- Reconocer HTML como lenguaje de marcado y las etiquetas como unidades de estructuración.
- Crear un documento HTML5 válido con `html`, `head`, `title` y `body`.

## Desarrollo de contenidos

## 1. ¿Qué es HTML?

HTML (*HyperText Markup Language*) es un lenguaje de marcado utilizado para describir la estructura y el significado del contenido de un documento web. No es un lenguaje de programación: no contiene por sí mismo la lógica habitual de un programa, sino que utiliza elementos y atributos para organizar información.

Una página web suele combinar varias tecnologías:

- **HTML:** estructura y significado del contenido.
- **CSS:** presentación visual y distribución.
- **JavaScript:** comportamiento e interacción programada.

En esta unidad nos centraremos en HTML. Una página puede tener HTML correcto aunque todavía no tenga colores, tipografías ni una maquetación atractiva.

## 2. Etiquetas, elementos y atributos

Una etiqueta suele escribirse entre los símbolos `<` y `>`. Muchos elementos tienen una etiqueta de apertura y otra de cierre:

```html
<p>Este es un párrafo.</p>
```

En el ejemplo, `<p>` es la etiqueta de apertura, `</p>` la de cierre y todo el conjunto constituye un **elemento**. El contenido está entre ambas etiquetas.

Algunos elementos son vacíos y no contienen texto ni una etiqueta de cierre, por ejemplo `<br>` o `<img>`.

Los atributos aportan información adicional al elemento y se escriben normalmente en la etiqueta de apertura:

```html
<p lang="es">Texto en español.</p>
```

`lang` es el atributo y `es` su valor.

## 3. Estructura mínima de HTML5

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi primera página</title>
</head>
<body>
    <h1>Mi primera página web</h1>
    <p>Estoy aprendiendo a estructurar documentos HTML.</p>
</body>
</html>
```

- `<!DOCTYPE html>` indica que el documento utiliza HTML moderno.
- `<html>` es el elemento raíz. `lang="es"` identifica el idioma principal.
- `<head>` contiene información sobre el documento que no forma parte del contenido principal visible.
- `<meta charset="UTF-8">` declara la codificación de caracteres.
- `<meta name="viewport">` ayuda a que el navegador adapte la anchura de la página al dispositivo.
- `<title>` define el título de la pestaña o ventana del navegador.
- `<body>` contiene el contenido del documento.

## 4. Qué ocurre cuando abrimos el archivo

El navegador interpreta el marcado y construye una representación estructurada del documento. No debemos confundir el código fuente con el resultado visual: el navegador procesa las etiquetas para presentar el contenido.

Un archivo HTML es texto plano y puede editarse con un editor de código. Se guarda con extensión `.html`, por ejemplo `index.html`.

## 5. Errores habituales

- Olvidar `<!DOCTYPE html>`.
- Colocar el contenido visible dentro de `<head>` en lugar de `<body>`.
- Omitir el cierre de elementos que lo necesitan.
- Escribir etiquetas con errores tipográficos.
- Guardar el archivo como `index.html.txt` por tener ocultas las extensiones.
- Utilizar HTML para intentar resolver cuestiones que corresponden a CSS.

## Ejemplo guiado

### Ejemplo guiado: ficha de presentación

Crea una carpeta `ud2` y dentro un archivo `index.html`. Escribe la estructura mínima anterior y cambia el título y el contenido por una breve presentación. Guarda el archivo y ábrelo en el navegador. Después modifica el texto, guarda de nuevo y actualiza la página.

## Actividades prácticas

### E01 · Reconocer las partes

Sobre el código de ejemplo, identifica `DOCTYPE`, elemento raíz, metadatos, título de pestaña y contenido visible. Explica con tus palabras para qué sirve cada parte.

### E02 · Documento desde cero

Crea `presentacion.html` con la estructura HTML5 mínima. Debe tener idioma español, codificación UTF-8, viewport, título y un contenido en el cuerpo.

### E03 · Detectar errores

Corrige un documento en el que `title` aparece dentro de `body`, el párrafo aparece dentro de `head` y falta el cierre de `html`. Explica cada corrección.

### E04 · Comprobación del navegador

Abre el archivo en el navegador. Cambia el título y el contenido, guarda y comprueba qué parte cambia en la pestaña y qué parte cambia en la página.

## Reto de aplicación

Crea una página de bienvenida para el módulo DIW. Debe incluir un título de pestaña descriptivo, idioma español y un mensaje de bienvenida dentro del cuerpo. No utilices CSS ni JavaScript.

## Errores que debes evitar

- Elegir etiquetas por su apariencia en lugar de por su significado.
- Escribir código sin revisar el anidamiento.
- Olvidar las etiquetas asociadas a los controles de formulario.
- Dar por válido un documento solo porque el navegador lo muestra.

## Resumen de la sesión

Al finalizar debes poder explicar los conceptos principales, construir un ejemplo pequeño y justificar las decisiones de marcado realizadas.

## Autoevaluación

- [ ] Sé explicar la diferencia entre HTML, CSS y JavaScript.
- [ ] Distingo etiqueta, elemento y atributo.
- [ ] Puedo crear la estructura mínima HTML5 sin copiarla.
- [ ] Sé dónde se coloca el contenido visible.

## Registro personal

- Dudas que me quedan:
- Errores que he corregido:
- Qué necesito practicar de nuevo:
