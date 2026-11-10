---
asignatura: DIW
unidad: UD2
sesion: 06
tipo: material-alumnado
estado: preparado
programacion: "UP2 - Estructura HTML y Semántica HTML5"
duracion: "55 minutos"
---

# Sesión 06 · Categorías de contenido HTML y organización del documento

> [!abstract] Propósito de la sesión
> Conocer las categorías de contenido indicadas en la programación y comprender que los elementos HTML tienen modelos de contenido y restricciones.

## Objetivos de aprendizaje
- Reconocer las categorías de metadatos, flujo e interactivos.
- Comprender que no todos los elementos admiten cualquier contenido.
- Detectar anidamientos y combinaciones inadecuadas.

## Desarrollo de contenidos

## 1. ¿Por qué existen categorías de contenido?

HTML define modelos y categorías para describir qué tipo de contenido representa un elemento y en qué contextos puede aparecer. Estas categorías ayudan a entender las reglas de anidamiento y la estructura del documento.

No es necesario memorizar todas las categorías y excepciones del estándar. En esta unidad trabajaremos las que aparecen en la programación y las utilizaremos para razonar sobre documentos reales.

## 2. Metadatos del documento

Los elementos de metadatos aportan información sobre el documento o relacionan recursos externos. Se encuentran habitualmente en `<head>`.

Ejemplos:

- `<title>`: título del documento.
- `<meta>`: metadatos como codificación o descripción.
- `<link>`: relación con un recurso externo, por ejemplo una hoja de estilos.
- `<style>`: reglas de estilo incrustadas en el documento.

En esta unidad identificaremos su función, aunque la aplicación de CSS se trabajará en la UD3.

## 3. Contenido de flujo

El contenido de flujo comprende la mayor parte de los elementos que aparecen dentro del cuerpo del documento: encabezados, párrafos, listas, secciones, artículos, formularios y muchos otros.

Ejemplos: `p`, `h1`, `ul`, `li`, `main`, `section`, `article`, `form`.

## 4. Contenido interactivo

Son elementos que permiten o representan interacción del usuario. Entre los ejemplos habituales se encuentran:

- `<a>` cuando tiene `href`.
- `<button>`.
- `<input>`.
- `<select>`.
- `<textarea>`.

Un elemento puede pertenecer a más de una categoría. Las categorías no siempre son compartimentos excluyentes.

## 5. Modelo de contenido y anidamiento

No basta con que una etiqueta esté bien escrita: también debe aparecer en un contexto permitido. Por ejemplo, un botón puede contener texto y otros contenidos permitidos, pero no debe contener otro botón. Un párrafo no debe contener elementos de bloque que rompan su modelo de contenido.

Ejemplo correcto:

```html
<p>Visita la <a href="https://example.com">página informativa</a>.</p>
```

Ejemplo incorrecto:

```html
<p>
    Información principal
    <div>Bloque anidado dentro del párrafo</div>
</p>
```

## 6. Validación del marcado

Un validador permite detectar errores de sintaxis, anidamiento y uso del estándar. No sustituye el razonamiento del desarrollador: un documento puede ser válido y aun así estar mal organizado o resultar poco claro.

La herramienta de referencia es el validador del W3C: https://validator.w3.org/ . Se puede validar por dirección web, archivo o entrada directa de código, según las opciones disponibles.

## 7. Idea clave

La validez responde a “¿respeta las reglas del lenguaje?”. La calidad semántica responde a “¿representa correctamente el significado del contenido?”. Son cuestiones relacionadas, pero no idénticas.

## Ejemplo guiado

### Ejemplo guiado: localizar categorías

En un documento HTML completo, marca con un color los elementos del `head`, con otro los elementos de flujo del `body` y con un tercero los elementos interactivos. Un mismo elemento puede tener más de una función o categoría; anota los casos que generen dudas.

## Actividades prácticas

### E21 · Clasificar elementos

Clasifica `title`, `meta`, `link`, `p`, `section`, `article`, `a`, `button`, `input`, `select` y `textarea`. Indica su ubicación habitual y función.

### E22 · ¿Puede anidarse?

Analiza ocho fragmentos HTML y determina si el anidamiento es adecuado. Justifica la respuesta sin limitarte a decir “funciona en mi navegador”.

### E23 · Validación de un documento

Valida un archivo HTML con el servicio W3C. Registra los errores, corrígelos y vuelve a validar. Entrega una breve lista de cambios.

### E24 · Válido y semántico

Compara dos documentos que muestran el mismo resultado aproximado, uno con elementos semánticos y otro con contenedores genéricos. Explica cuál comunica mejor la estructura y por qué.

## Reto de aplicación

Prepara un documento HTML con errores deliberados de anidamiento. Intercámbialo con otra persona para que lo valide, localice los errores y proponga correcciones.

## Errores que debes evitar

- Elegir etiquetas por su apariencia en lugar de por su significado.
- Escribir código sin revisar el anidamiento.
- Olvidar las etiquetas asociadas a los controles de formulario.
- Dar por válido un documento solo porque el navegador lo muestra.

## Resumen de la sesión

Al finalizar debes poder explicar los conceptos principales, construir un ejemplo pequeño y justificar las decisiones de marcado realizadas.

## Autoevaluación

- [ ] Reconozco metadatos, contenido de flujo e interactivo.
- [ ] Entiendo que las categorías pueden solaparse.
- [ ] Sé que las reglas de anidamiento dependen del elemento.
- [ ] Puedo utilizar un validador y corregir los errores que informa.

## Registro personal

- Dudas que me quedan:
- Errores que he corregido:
- Qué necesito practicar de nuevo:
