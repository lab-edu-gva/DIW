# Ejercicio 3: Creación guiada de una tarjeta de usuario con HTML5 y CSS3

## 1. Objetivo

Crear una tarjeta de usuario que incluya una imagen, un nombre, una descripción y un enlace con apariencia de botón.

Aprenderás a utilizar HTML semántico, selectores CSS, el modelo de cajas y pseudoclases.

## 2. Preparación del proyecto

Crea una carpeta llamada `ejercicio-tarjeta` con los siguientes archivos:

- `index.html`
- `estilos.css`

## 3. Paso 1. Construye el HTML

Abre `index.html` y crea la estructura básica de un documento HTML5.

Debes cumplir estos requisitos:

1. Indica que el documento utiliza HTML5.
2. Establece el idioma del documento en español.
3. Configura la codificación de caracteres para mostrar correctamente tildes y eñes.
4. Configura la página para adaptarse al ancho de los dispositivos.
5. Establece como título de la pestaña del navegador `Mi tarjeta de usuario`.
6. Enlaza el archivo externo `estilos.css`.
7. Dentro de `<body>`, crea un elemento `<article>` con la clase `tarjeta`.

Dentro del artículo, añade los siguientes elementos y en este orden:

### Imagen

- Utiliza la etiqueta `<img>`.
- Como dirección de imagen, utiliza `https://placehold.co/280x160`.
- Añade el atributo `alt` con el texto `Imagen de perfil del usuario`.
- Asigna la clase `tarjeta-imagen`.

### Título

- Añade un encabezado de nivel 2 con el nombre `María García`.

### Descripción

- Añade un párrafo con el siguiente texto: `Desarrolladora web especializada en HTML, CSS y diseño de interfaces.`

### Enlace

- Añade un enlace con el texto `Ver perfil`.
- Como destino, utiliza `https://example.com`.
- Asígnale la clase `boton`.

Guarda el archivo y ábrelo en el navegador. Comprueba que aparecen todos los elementos, aunque todavía no tengan el diseño definitivo.

## 4. Paso 2. Configura el aspecto general de la página

Abre `estilos.css`. Escribe una regla CSS para seleccionar el elemento `body`.

Añade las siguientes declaraciones, una por línea:

1. Establece el tipo de letra en Arial, utilizando una familia genérica sans-serif como alternativa.
2. Cambia el fondo de la página a gris claro, utilizando el color hexadecimal `#f2f4f8`.
3. Elimina el margen exterior predeterminado del navegador.
4. Establece un relleno interior de 40 píxeles arriba y abajo, y de 20 píxeles a izquierda y derecha.

**Comprueba:** el fondo debe ser gris claro y el contenido debe dejar espacio respecto a los bordes de la ventana.

## 5. Paso 3. Diseña la tarjeta

Crea una regla CSS que seleccione cualquier elemento que tenga la clase `tarjeta`.

Escribe una declaración por cada uno de los siguientes requisitos:

1. Limita el ancho máximo de la tarjeta a 320 píxeles.
2. Haz que el ancho incluya el contenido, el relleno y los bordes.
3. Elimina el margen superior e inferior y deja que el navegador calcule automáticamente los márgenes izquierdo y derecho para centrar la tarjeta.
4. Añade 20 píxeles de relleno en los cuatro lados.
5. Establece el fondo en blanco mediante el color hexadecimal `#ffffff`.
6. Añade un borde de 1 píxel, línea continua y color `#dddddd`.
7. Redondea las esquinas con un radio de 8 píxeles.
8. Centra horizontalmente el texto que contiene la tarjeta.

**Comprueba:** la tarjeta debe aparecer centrada, con fondo blanco, borde gris y esquinas redondeadas.

## 6. Paso 4. Da formato a la imagen

Crea una regla CSS para seleccionar el elemento que tenga la clase `tarjeta-imagen`.

Añade estas declaraciones:

1. Haz que la imagen ocupe el 100 % del ancho disponible.
2. Configura su altura para que se calcule automáticamente y conserve sus proporciones.
3. Redondea las esquinas de la imagen con un radio de 6 píxeles.

**Comprueba:** la imagen debe ajustarse al ancho interior de la tarjeta sin deformarse.

## 7. Paso 5. Personaliza el título

Crea un selector que afecte únicamente a los encabezados `<h2>` que estén dentro de un elemento con la clase `tarjeta`.

Añade estas declaraciones:

1. Establece el color del texto en azul oscuro, con el hexadecimal `#243b53`.
2. Asigna un margen superior de 15 píxeles.

**Comprueba:** el nombre debe aparecer en azul oscuro y separado de la imagen.

## 8. Paso 6. Personaliza la descripción

Crea un selector que afecte únicamente a los párrafos que estén dentro de la tarjeta.

Añade estas declaraciones:

1. Establece el color del texto en `#52606d`.
2. Establece la altura de línea en 1,5 veces el tamaño de la fuente.

**Comprueba:** el texto debe ser legible y tener una separación cómoda entre líneas.

## 9. Paso 7. Convierte el enlace en un botón

Crea una regla CSS para seleccionar los elementos que tengan la clase `boton`.

Añade las siguientes declaraciones:

1. Configura el enlace para que se comporte como un elemento `inline-block`.
2. Establece un relleno de 10 píxeles arriba y abajo, y de 20 píxeles a izquierda y derecha.
3. Establece el fondo azul corporativo con el hexadecimal `#0066cc`.
4. Cambia el color del texto a blanco mediante `#ffffff`.
5. Elimina la decoración del texto para que el enlace no aparezca subrayado.
6. Redondea las esquinas con un radio de 5 píxeles.

**Comprueba:** el enlace debe tener aspecto de botón azul, con texto blanco y esquinas redondeadas.

## 10. Paso 8. Añade el efecto hover

Crea una nueva regla CSS que seleccione el enlace cuando el puntero del ratón se encuentre encima de él.

Dentro de esta regla:

1. Modifica únicamente el color de fondo.
2. Utiliza el color hexadecimal `#004c99`.

No modifiques el color del texto ni las dimensiones del botón.

**Comprueba:**

- Cuando el ratón no está encima, el botón debe ser azul.
- Cuando el ratón está encima, debe cambiar a azul oscuro.
- Cuando retiras el ratón, debe recuperar su color original.

## 11. Paso 9. Valida el CSS

Accede al [Validador oficial de CSS del W3C](https://jigsaw.w3.org/css-validator/).

1. Abre el archivo `estilos.css`.
2. Copia su contenido y pégalo en la opción de validación por entrada directa de texto.
3. Ejecuta la validación.
4. Si aparecen errores, corrige el código y vuelve a validarlo.

Ten en cuenta que una advertencia no siempre implica que el CSS sea incorrecto: lee el mensaje antes de modificar el código.

## 12. Paso 10. Lista de comprobación

Antes de entregar, verifica los siguientes puntos:

- [ ] El documento HTML está correctamente estructurado.
- [ ] Se utiliza la etiqueta semántica `<article>`.
- [ ] La imagen tiene un atributo `alt`.
- [ ] El HTML enlaza correctamente el archivo CSS.
- [ ] La tarjeta tiene un ancho máximo de 320 píxeles.
- [ ] La tarjeta está centrada y tiene 20 píxeles de relleno.
- [ ] La imagen conserva sus proporciones.
- [ ] El título y el párrafo tienen los colores indicados.
- [ ] El enlace tiene apariencia de botón.
- [ ] El botón cambia de color mediante `:hover`.
- [ ] El CSS se ha validado con el W3C.

## 13. Preguntas de reflexión

Responde con tus propias palabras:

1. ¿Qué diferencia hay entre `margin` y `padding`?
2. ¿Qué ventaja ofrece `box-sizing: border-box`?
3. ¿Por qué utilizamos una clase para identificar la tarjeta?
4. ¿Qué diferencia existe entre un enlace HTML y un botón HTML?
5. ¿Qué función desempeña la pseudoclase `:hover`?
6. ¿Qué sucede si eliminamos la declaración que quita el subrayado del enlace?

## 14. Entrega en Aules

La carpeta del proyecto debe contener:

- `index.html`
- `estilos.css`
- `README.md`

Comprime la carpeta en un archivo llamado `ejercicio-tarjeta.zip` y súbelo a la tarea correspondiente de Aules.

**Importante:** no se trata de copiar un diseño terminado, sino de construirlo declaración a declaración y comprender para qué sirve cada propiedad CSS.