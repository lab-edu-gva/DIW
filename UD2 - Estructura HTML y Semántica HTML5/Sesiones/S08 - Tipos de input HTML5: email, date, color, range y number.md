---
asignatura: DIW
unidad: UD2
sesion: 08
tipo: material-alumnado
estado: preparado
programacion: "UP2 - Estructura HTML y Semántica HTML5"
duracion: "55 minutos"
---

# Sesión 08 · Tipos de input HTML5: email, date, color, range y number

> [!abstract] Propósito de la sesión
> Seleccionar el tipo de control adecuado al dato que se desea recoger.

## Objetivos de aprendizaje
- Distinguir tipos de `input` habituales de HTML5.
- Aplicar `email`, `date`, `color`, `range` y `number`.
- Elegir controles coherentes con la naturaleza del dato.

## Desarrollo de contenidos

## 1. El atributo `type`

El elemento `<input>` puede representar controles diferentes según el valor de `type`. Elegir el tipo correcto mejora la experiencia de uso y permite al navegador aplicar comportamientos y validaciones apropiados.

## 2. Correo electrónico: `email`

```html
<label for="correo">Correo electrónico:</label>
<input type="email" id="correo" name="correo">
```

El navegador puede comprobar que el valor tenga un formato de correo reconocible. Esta comprobación no garantiza que la dirección exista ni que pertenezca a la persona.

## 3. Fecha: `date`

```html
<label for="nacimiento">Fecha:</label>
<input type="date" id="nacimiento" name="nacimiento">
```

El navegador puede mostrar un selector de fecha. La presentación concreta depende del navegador y del sistema.

## 4. Color: `color`

```html
<label for="color-favorito">Color:</label>
<input type="color" id="color-favorito" name="color-favorito" value="#3366cc">
```

Permite seleccionar un color mediante el control que ofrezca el navegador. El valor suele representarse como un color hexadecimal.

## 5. Número: `number`

```html
<label for="edad">Edad:</label>
<input type="number" id="edad" name="edad" min="0" max="120" step="1">
```

Permite introducir valores numéricos. `min`, `max` y `step` delimitan el rango y el incremento permitido.

## 6. Rango: `range`

```html
<label for="satisfaccion">Satisfacción:</label>
<input type="range" id="satisfaccion" name="satisfaccion" min="0" max="10" step="1" value="5">
```

Presenta un control deslizante. Es apropiado para seleccionar un valor dentro de un intervalo, especialmente cuando no se necesita una precisión de escritura elevada.

## 7. Comparación rápida

| Tipo | Dato | Uso habitual |
|---|---|---|
| `email` | Correo | Contacto o registro |
| `date` | Fecha | Citas o fechas de nacimiento |
| `color` | Color | Preferencias visuales |
| `number` | Número | Cantidades o edades |
| `range` | Valor dentro de un intervalo | Valoraciones o ajustes |

## 8. Elegir con criterio

No todos los campos numéricos deben ser `number`: un código postal, un teléfono o un identificador pueden contener ceros iniciales o símbolos y no representan una cantidad sobre la que se hagan operaciones. La elección del tipo debe responder al significado del dato, no solo a su apariencia.

## Ejemplo guiado

### Ejemplo guiado: preferencias de usuario

Crea un formulario con correo electrónico, fecha preferida, color favorito, número de participantes y nivel de satisfacción de 0 a 10. Añade etiquetas visibles y valores mínimos/máximos cuando proceda.

## Actividades prácticas

### E29 · Elegir el tipo correcto

Para una lista de datos (correo, fecha de cita, edad, color, nivel de satisfacción, teléfono y código postal), selecciona un tipo adecuado y justifica los casos en que `number` no conviene.

### E30 · Construir controles

Crea cinco controles, uno por cada tipo estudiado. Todos deben tener `id`, `name` y `label` asociado.

### E31 · Rangos y pasos

Configura un control de número de 1 a 30 con incrementos de 1 y un rango de 0 a 100 con incrementos de 5. Comprueba su comportamiento.

### E32 · Prueba de navegador

Abre el formulario en dos navegadores o dispositivos si es posible. Compara cómo se presentan `date`, `color` y `range` y registra las diferencias.

## Reto de aplicación

Diseña un formulario de preferencias para una plataforma de cursos. Debe recoger correo, fecha de inicio, color de interfaz, número de horas semanales y nivel de dificultad preferido.

## Errores que debes evitar

- Elegir etiquetas por su apariencia en lugar de por su significado.
- Escribir código sin revisar el anidamiento.
- Olvidar las etiquetas asociadas a los controles de formulario.
- Dar por válido un documento solo porque el navegador lo muestra.

## Resumen de la sesión

Al finalizar debes poder explicar los conceptos principales, construir un ejemplo pequeño y justificar las decisiones de marcado realizadas.

## Autoevaluación

- [ ] Sé elegir el `type` en función del dato.
- [ ] Distingo `number` y `range`.
- [ ] Configuro `min`, `max` y `step`.
- [ ] Comprendo que el comportamiento visual depende del navegador.

## Registro personal

- Dudas que me quedan:
- Errores que he corregido:
- Qué necesito practicar de nuevo:
