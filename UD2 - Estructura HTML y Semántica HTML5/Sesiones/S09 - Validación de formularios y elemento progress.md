---
asignatura: DIW
unidad: UD2
sesion: 09
tipo: material-alumnado
estado: preparado
programacion: "UP2 - Estructura HTML y Semántica HTML5"
duracion: "55 minutos"
---

# Sesión 09 · Validación de formularios y elemento progress

> [!abstract] Propósito de la sesión
> Aplicar restricciones de validación HTML5 y representar el avance de una tarea con `progress`.

## Objetivos de aprendizaje
- Utilizar atributos de validación habituales.
- Comprender los límites de la validación en cliente.
- Distinguir `progress` de otros elementos de formulario.

## Desarrollo de contenidos

## 1. Validar antes de enviar

La validación permite comprobar si los datos introducidos cumplen determinadas condiciones antes de enviar el formulario. HTML ofrece atributos que permiten definir restricciones sin escribir JavaScript.

## 2. Atributos de validación

- `required`: obliga a completar el campo.
- `minlength` y `maxlength`: establecen longitudes mínima y máxima de texto.
- `min` y `max`: establecen límites para valores numéricos o fechas compatibles.
- `step`: establece los incrementos admitidos en controles numéricos.
- `pattern`: define un patrón que debe cumplir el valor de determinados campos de texto.
- `type`: puede activar comprobaciones propias del tipo, como en `email`.

Ejemplo:

```html
<label for="usuario">Usuario:</label>
<input type="text" id="usuario" name="usuario"
       required minlength="4" maxlength="16">

<label for="correo">Correo:</label>
<input type="email" id="correo" name="correo" required>
```

## 3. Validación numérica

```html
<label for="plazas">Número de plazas:</label>
<input type="number" id="plazas" name="plazas"
       min="1" max="25" step="1" required>
```

El navegador puede impedir el envío si el valor no cumple los límites establecidos.

## 4. Patrones con `pattern`

`pattern` utiliza una expresión regular para definir el formato admitido en determinados controles de texto. Ejemplo sencillo para un código de cinco dígitos:

```html
<label for="codigo">Código:</label>
<input type="text" id="codigo" name="codigo"
       pattern="[0-9]{5}" required>
```

El patrón debe describirse y probarse con cuidado. No conviene crear expresiones complejas sin comprenderlas. Además, el atributo `title` puede ayudar a explicar el formato esperado, pero la instrucción principal debe estar visible junto al campo.

## 5. Validación en cliente y en servidor

La validación HTML mejora la experiencia, pero no garantiza la seguridad ni la integridad de los datos. Cualquier usuario puede modificar el HTML desde las herramientas del navegador o enviar peticiones sin utilizar el formulario.

Por tanto, una aplicación real debe validar también en el servidor. La validación del navegador es una ayuda, no una frontera de seguridad.

## 6. Elemento `progress`

`<progress>` representa el progreso de una tarea:

```html
<label for="avance">Progreso de la instalación:</label>
<progress id="avance" value="70" max="100">70 %</progress>
```

- `value` indica el progreso actual.
- `max` indica el valor máximo.
- El texto interior puede servir como contenido alternativo en navegadores que no representen el elemento.

No debe confundirse con `meter`, que representa una medida dentro de un rango, no el avance de una tarea.

## 7. Errores frecuentes

- Pensar que `required` sustituye a la validación del servidor.
- Utilizar `pattern` sin explicar al usuario el formato esperado.
- Poner `min` y `max` en un campo que no admite esos atributos.
- Utilizar `progress` como si fuera una barra de valoración o una medida estadística.

## Ejemplo guiado

### Ejemplo guiado: inscripción validada

Amplía el formulario de inscripción: nombre obligatorio, correo obligatorio, usuario de entre 4 y 16 caracteres, número de participantes entre 1 y 25 y código de cinco dígitos. Añade un `progress` que muestre el 60 % de una tarea ficticia.

## Actividades prácticas

### E33 · Relacionar atributos

Asocia cada requisito con el atributo adecuado: campo obligatorio, longitud mínima, longitud máxima, número máximo, incremento y patrón de cinco cifras.

### E34 · Validar un formulario

Añade validaciones a un formulario de registro. Prueba valores correctos e incorrectos y anota qué mensajes muestra el navegador.

### E35 · Patrón de código

Configura un campo que acepte exactamente cinco dígitos. Prueba valores de cuatro, cinco y seis caracteres, letras y espacios.

### E36 · Barra de progreso

Crea tres barras de progreso con valores 20/100, 65/100 y 100/100. Añade etiquetas descriptivas y explica qué representa cada una.

## Reto de aplicación

Construye un formulario de inscripción completo con al menos cuatro restricciones de validación distintas y una barra `progress` que represente el avance de la inscripción. Añade una explicación de por qué el servidor debe validar de nuevo.

## Errores que debes evitar

- Elegir etiquetas por su apariencia en lugar de por su significado.
- Escribir código sin revisar el anidamiento.
- Olvidar las etiquetas asociadas a los controles de formulario.
- Dar por válido un documento solo porque el navegador lo muestra.

## Resumen de la sesión

Al finalizar debes poder explicar los conceptos principales, construir un ejemplo pequeño y justificar las decisiones de marcado realizadas.

## Autoevaluación

- [ ] Sé utilizar `required`, `minlength`, `maxlength`, `min`, `max`, `step` y `pattern`.
- [ ] Puedo probar restricciones con valores correctos e incorrectos.
- [ ] Entiendo que la validación del navegador no sustituye a la del servidor.
- [ ] Sé representar el avance con `progress`.

## Registro personal

- Dudas que me quedan:
- Errores que he corregido:
- Qué necesito practicar de nuevo:
