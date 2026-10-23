
# Reto de Depuración CSS: Bug Hunter & Box Model Fix

**Módulo:** Diseño de Interfaces Web (DIW) — 2.º DAW  
**Unidad de Programación:** UP3 – Estilos CSS y Modelo de Cajas  
**Resultado de Aprendizaje:** RA2 – Crea interfaces web homogéneas definiendo y aplicando estilos.  
**Modalidad:** Trabajo individual  
**Entrega:** Plataforma Aules

---

## 1. Contexto de la misión

¡Bienvenido al equipo de desarrollo web!

Has recibido un proyecto que contiene una tarjeta de producto con varios errores de diseño. La tarjeta se desborda de su contenedor, la etiqueta de oferta aparece en una posición incorrecta y el botón de compra no respeta los espacios verticales esperados.

Tu misión consiste en **investigar, localizar y corregir cuatro errores de CSS** sin rehacer la página desde cero.

Para ello, deberás utilizar las herramientas de desarrollo del navegador (F12) y analizar cómo afectan las propiedades CSS al modelo de cajas (*Box Model*).

## 2. Objetivos

Al finalizar el ejercicio, deberás ser capaz de:

- Interpretar el modelo de cajas de CSS.
- Diferenciar entre `content`, `padding`, `border` y `margin`.
- Comprender cómo afecta `box-sizing` al tamaño de los elementos.
- Utilizar `position: relative` y `position: absolute` para posicionar elementos.
- Identificar cuándo es necesario aplicar `display: inline-block`.
- Utilizar las herramientas de desarrollo del navegador para depurar CSS.

## 3. Preparación del proyecto

Crea una carpeta llamada `reto-box-model` con los siguientes archivos:

- `index.html`
- `estilos.css`

Copia en ellos el código inicial proporcionado por el profesor, **sin modificarlo inicialmente**.

Abre `index.html` en el navegador y observa el resultado. No intentes corregir los errores a ciegas: primero debes investigar qué está ocurriendo.

## 4. Desarrollo del reto

### Fase 1. Investigación con las herramientas de desarrollo

Abre las herramientas de desarrollo pulsando F12 o haciendo clic derecho sobre la página y seleccionando «Inspeccionar».

Examina los siguientes elementos:

- `.contenedor-padre`
- `.tarjeta-producto`
- `.badge-nuevo`
- `.btn-comprar`

Utiliza el inspector para consultar sus propiedades CSS, sus dimensiones y el diagrama del modelo de cajas.

### Fase 2. Localización de los errores

Encuentra los cuatro errores de diseño y documenta cada uno respondiendo a estas preguntas:

1. ¿Qué comportamiento incorrecto observas?
2. ¿Qué propiedad o propiedades CSS lo provocan?
3. ¿Por qué se produce el problema?
4. ¿Qué modificación realizarías para solucionarlo?

No basta con cambiar una propiedad hasta que parezca funcionar: debes explicar por qué la solución es correcta.

### Fase 3. Corrección del código

Modifica `estilos.css` para conseguir que la tarjeta cumpla los siguientes requisitos:

- La tarjeta debe quedar dentro de su contenedor, sin desbordamiento horizontal.
- La insignia «¡OFERTA!» debe posicionarse respecto a la tarjeta del producto.
- El botón «Añadir al Carrito» debe respetar la separación vertical respecto al contenido anterior.
- El tamaño de los elementos debe ajustarse correctamente al espacio disponible, teniendo en cuenta el modelo de cajas.

Conserva la estructura HTML original y realiza las modificaciones necesarias únicamente en CSS.

### Fase 4. Comprobación final

Cuando termines:

1. Recarga la página y comprueba el resultado.
2. Vuelve a inspeccionar los elementos con F12.
3. Comprueba las dimensiones de la tarjeta y del contenedor.
4. Verifica la posición de la insignia y el comportamiento del botón.
5. Asegúrate de que no existe desbordamiento horizontal.

## Fase 5. Normas del reto

- Trabaja de forma individual.
- No reconstruyas la página desde cero.
- No elimines elementos para ocultar los errores.
- Utiliza las herramientas de desarrollo del navegador para investigar.
- Justifica técnicamente las modificaciones realizadas.
- Puedes consultar la documentación oficial de CSS, pero debes comprender y explicar tus soluciones.

---

**¡Misión cumplida cuando la tarjeta funcione correctamente y puedas explicar por qué!**

Recuerda: en CSS, si algo se sale de su sitio, no siempre necesita más espacio. A veces necesita que alguien le explique cómo funcionan las cajas.

