
# Bienvenida a la primera sesión: Introducción a CSS

¡Bienvenidos y bienvenidas!

En esta primera sesión vamos a comenzar a trabajar con **CSS (Cascading Style Sheets)**, el lenguaje que utilizamos para definir la apariencia visual de las páginas web creadas con HTML.

HTML nos permite estructurar el contenido de una página, mientras que CSS nos permite decidir cómo se presenta: colores, tipografías, tamaños, espacios, bordes y distribución de los elementos.

Durante la sesión realizaremos **tres ejercicios prácticos**, aumentando progresivamente la dificultad. Empezaremos por los fundamentos y terminaremos creando una tarjeta de usuario con un diseño atractivo.

## Objetivos de la sesión

Al finalizar la clase, deberás ser capaz de:

- Crear y vincular una hoja de estilos externa.
- Aplicar selectores, clases y propiedades CSS.
- Comprender el modelo de cajas (*Box Model*).
- Diferenciar entre `content-box` y `border-box`.
- Diseñar una tarjeta utilizando HTML semántico y CSS.
- Inspeccionar elementos mediante las herramientas de desarrollo del navegador.
- Validar una hoja de estilos con el validador oficial del W3C.

## Ejercicio 1: Creación y vinculación de una hoja de estilos externa

**Nivel:** Inicial  
**Duración estimada:** 20 minutos

### Objetivo

Practicar la sintaxis básica de CSS y aprender a vincular correctamente una hoja de estilos externa con un documento HTML.

### ¿Qué vamos a hacer?

- Crear una carpeta llamada `Practica_CSS_01`.
- Crear un archivo `index.html` con una estructura semántica básica que incluya `<header>`, `<main>` y `<footer>`.
- Crear un archivo externo llamado `estilos.css` y vincularlo desde el HTML.
- Cambiar el fondo de la página a gris claro mediante el color `#f4f4f4`.
- Establecer Arial como tipografía principal, con una alternativa genérica sans-serif.
- Crear una clase llamada `.titulo-destacado` que muestre el texto en azul oscuro y con un tamaño de 24 píxeles.
- Aplicar esa clase al encabezado principal `<h1>`.

**Resultado esperado:** una página HTML sencilla con estilos definidos en un archivo CSS independiente.

## Ejercicio 2: Dominando el modelo de cajas (*Box Model*)

**Nivel:** Intermedio  
**Duración estimada:** 40 minutos

### Objetivo

Comprender de forma visual la diferencia entre `content-box` y `border-box`, dos valores de la propiedad CSS `box-sizing`.

### ¿Qué vamos a hacer?

1. Crear dos contenedores `<section>` con la clase `caja-test`.
2. Añadir un párrafo descriptivo dentro de cada contenedor.
3. Aplicar a ambas cajas las mismas propiedades:
   - Ancho: `300px`.
   - Relleno interior: `25px`.
   - Borde: `5px solid #333`.
   - Margen exterior: `20px`.
   - Fondo blanco: `#ffffff`.
4. Configurar la primera caja con `box-sizing: content-box`.
5. Configurar la segunda caja con `box-sizing: border-box`.
6. Inspeccionar ambas cajas con las herramientas de desarrollo del navegador, accesibles normalmente mediante F12.

### Cuestión de reflexión

- ¿Cuál es el ancho total de cada caja, sin contar los márgenes?
- ¿Por qué tienen anchuras diferentes si ambas tienen `width: 300px`?
- ¿Qué ventajas ofrece utilizar `border-box` al diseñar páginas web?

Explica tus conclusiones mediante comentarios en el archivo CSS.

**Resultado esperado:** dos cajas visualmente diferentes que permitan comprender cómo se calcula su anchura.

## Ejercicio 3: Maquetación de tarjetas de producto o perfil

**Nivel:** Avanzado  
**Duración estimada:** 40 minutos

### Objetivo

Aplicar los conocimientos adquiridos para construir una tarjeta de usuario o producto utilizando HTML semántico y CSS.

### ¿Qué vamos a hacer?

Crear una tarjeta utilizando la etiqueta `<article>` que incluya:

- Una imagen de cabecera o avatar.
- Un título `<h2>` con el nombre.
- Un párrafo `<p>` descriptivo.
- Un enlace `<a>` con apariencia de botón.

### Requisitos de diseño

La tarjeta deberá cumplir estas condiciones:

- Tener un ancho máximo de `320px`.
- Estar centrada horizontalmente mediante `margin: 0 auto`.
- Utilizar `box-sizing: border-box`.
- Tener bordes redondeados de `8px`.
- Disponer de un relleno interior de `20px`.
- Mostrar el enlace como `inline-block`.
- Incluir relleno, un color de fondo corporativo y texto sin subrayado.
- Incorporar un efecto visual al pasar el cursor por encima del enlace mediante la pseudoclase `:hover`.

### Validación y entrega

1. Comprueba que el diseño se visualiza correctamente en el navegador.
2. Valida el archivo CSS utilizando el [Validador oficial de CSS del W3C](https://jigsaw.w3.org/css-validator/).
3. Corrige los errores que se detecten y vuelve a validar.
4. Organiza los archivos del proyecto en una carpeta.
5. Comprime la carpeta en un archivo `.zip`.
6. Entrega el archivo comprimido en la tarea correspondiente del aula virtual **Aules**.

**Resultado esperado:** una tarjeta de usuario o producto centrada, con imagen, título, descripción y un enlace con apariencia de botón.

## Planificación de la sesión

| Actividad | Duración |
|---|---:|
| Ejercicio 1: Hoja de estilos externa | 20 min |
| Ejercicio 2: Modelo de cajas | 40 min |
| Ejercicio 3: Tarjeta de usuario | 40 min |
| **Total de trabajo práctico** | **100 min** |

Las duraciones son orientativas. El ritmo de trabajo dependerá de las dudas y dificultades que aparezcan durante la sesión.

## Recomendaciones para trabajar

- Escribe el código tú mismo: evita copiar soluciones completas.
- Guarda los cambios con frecuencia.
- Comprueba el resultado en el navegador después de cada modificación.
- Lee los mensajes de error antes de intentar corregirlos.
- Pregunta cuando no entiendas una propiedad o su comportamiento.
- Utiliza nombres de clases claros y mantén el código bien organizado.

## Conclusión

Hoy empezamos a transformar páginas HTML sencillas en interfaces visualmente atractivas.

Primero aprenderemos a conectar HTML y CSS; después entenderemos cómo se calculan los tamaños de los elementos; finalmente, construiremos un componente web completo.

**La programación se aprende practicando, equivocándose y entendiendo por qué algo funciona.** Si a la primera no sale, no pasa nada: el navegador no pone notas.
