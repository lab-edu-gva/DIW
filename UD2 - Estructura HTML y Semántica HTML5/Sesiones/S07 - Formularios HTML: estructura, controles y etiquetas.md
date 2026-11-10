---
asignatura: DIW
unidad: UD2
sesion: 07
tipo: material-alumnado
estado: preparado
programacion: "UP2 - Estructura HTML y Semántica HTML5"
duracion: "55 minutos"
---

# Sesión 07 · Formularios HTML: estructura, controles y etiquetas

> [!abstract] Propósito de la sesión
> Crear formularios comprensibles mediante `form`, `label`, `input`, `select` y `textarea`.

## Objetivos de aprendizaje
- Reconocer la finalidad de un formulario HTML.
- Relacionar etiquetas descriptivas con sus controles.
- Crear formularios con campos de texto, selección y texto multilínea.

## Desarrollo de contenidos

## 1. Para qué sirve un formulario

Un formulario permite recoger datos introducidos por el usuario: una solicitud, una inscripción, una búsqueda o una encuesta. HTML proporciona los elementos para construir los controles; el procesamiento de los datos requiere un destino o una aplicación que los reciba.

## 2. Elemento `form`

`<form>` agrupa controles que forman parte de un envío. Entre sus atributos habituales se encuentran:

- `action`: dirección a la que se envían los datos.
- `method`: método HTTP utilizado para el envío, habitualmente `get` o `post`.

```html
<form action="/inscripcion" method="post">
    <!-- Controles del formulario -->
</form>
```

Un formulario no envía datos a ningún sitio útil si no existe un destino que los procese. En los ejercicios de esta unidad podremos trabajar con formularios de demostración sin backend.

## 3. `label` e `input`

`<input>` crea distintos tipos de controles según el atributo `type`. Es fundamental asociar una etiqueta descriptiva a cada campo.

```html
<label for="nombre">Nombre:</label>
<input type="text" id="nombre" name="nombre">
```

El valor de `for` debe coincidir con el `id` del control. `name` identifica el dato cuando se envía el formulario. `id` y `name` no son intercambiables: pueden coincidir en valor, pero cumplen funciones distintas.

## 4. Selección con `select` y `option`

```html
<label for="ciclo">Ciclo formativo:</label>
<select id="ciclo" name="ciclo">
    <option value="smr">SMR</option>
    <option value="daw">DAW</option>
    <option value="asir">ASIR</option>
</select>
```

Cada `<option>` representa una opción. El atributo `value` determina el dato asociado a la opción.

## 5. Texto multilínea con `textarea`

```html
<label for="observaciones">Observaciones:</label>
<textarea id="observaciones" name="observaciones" rows="4" cols="40"></textarea>
```

A diferencia de `input`, `textarea` permite introducir varias líneas. El contenido inicial se escribe entre la etiqueta de apertura y la de cierre.

## 6. Agrupar controles

`fieldset` permite agrupar controles relacionados y `legend` proporciona el título del grupo:

```html
<fieldset>
    <legend>Datos de contacto</legend>
    <label for="correo">Correo:</label>
    <input type="email" id="correo" name="correo">
</fieldset>
```

## 7. Errores habituales

- Crear controles sin `label`.
- Asociar un `label` a un `id` inexistente.
- Olvidar `name` cuando se necesita enviar el dato.
- Utilizar `textarea` como si fuera una etiqueta autocerrada.
- Confundir la construcción del formulario con el procesamiento del envío.

## Ejemplo guiado

### Ejemplo guiado: formulario de contacto

Construye un formulario con nombre, correo, ciclo formativo y observaciones. Asocia cada control con su `label`. Añade `fieldset` y `legend` para agrupar los datos. No es necesario implementar un servidor.

## Actividades prácticas

### E25 · Anatomía de un formulario

Identifica `form`, `action`, `method`, `label`, `input`, `name`, `id`, `select`, `option` y `textarea` en un ejemplo. Explica la función de cada uno.

### E26 · Asociar etiquetas

Recibe un formulario sin etiquetas correctamente asociadas. Corrige los `for` y los `id`, y añade los atributos `name` que falten.

### E27 · Formulario de inscripción

Crea un formulario de inscripción con nombre, apellidos, correo, ciclo y observaciones. Agrupa los campos en bloques lógicos.

### E28 · Inspección del envío

Explica qué información identifica `name`, qué hace `action` y qué diferencia general existe entre `get` y `post`. Indica qué parte necesita un servidor.

## Reto de aplicación

Diseña un formulario de solicitud de información para el centro. Incluye datos personales básicos, una selección de ciclo y un campo de observaciones. Todos los controles deben tener etiqueta asociada.

## Errores que debes evitar

- Elegir etiquetas por su apariencia en lugar de por su significado.
- Escribir código sin revisar el anidamiento.
- Olvidar las etiquetas asociadas a los controles de formulario.
- Dar por válido un documento solo porque el navegador lo muestra.

## Resumen de la sesión

Al finalizar debes poder explicar los conceptos principales, construir un ejemplo pequeño y justificar las decisiones de marcado realizadas.

## Autoevaluación

- [ ] Sé para qué sirve `form`.
- [ ] Distingo `id` y `name`.
- [ ] Asocio correctamente `label` e `input`.
- [ ] Sé utilizar `select`, `option` y `textarea`.

## Registro personal

- Dudas que me quedan:
- Errores que he corregido:
- Qué necesito practicar de nuevo:
