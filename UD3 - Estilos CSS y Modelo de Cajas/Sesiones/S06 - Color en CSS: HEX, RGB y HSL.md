# S06 · Color en CSS: HEX, RGB y HSL

---
asignatura: DIW
unidad: UD3
sesion: 6
tipo: material-alumnado
estado: preparado
publicar: true
---

## 1. El color como información

El color puede establecer jerarquías, identificar estados y reforzar una identidad visual. No debe ser el único medio para comunicar información: un error, por ejemplo, también debe identificarse mediante texto o un icono comprensible.

## 2. Palabras clave

CSS admite nombres de colores:

```css
h1 {
    color: navy;
}
```

Son cómodos para ejemplos, pero una paleta de proyecto suele necesitar valores precisos y documentados.

## 3. Notación hexadecimal

La forma habitual es `#RRGGBB`:
- Los dos primeros dígitos representan rojo.
- Los dos siguientes, verde.
- Los dos últimos, azul.
- Cada canal puede tomar valores hexadecimales entre `00` y `FF`.

Ejemplos:

```css
body {
    background-color: #ffffff;
}

h1 {
    color: #183153;
}

.aviso {
    background-color: #fff3cd;
}
```

La forma abreviada `#RGB` permite escribir ciertos colores con tres dígitos cuando cada pareja de canales repite el mismo dígito.

## 4. RGB y RGBA

RGB expresa la intensidad de rojo, verde y azul:

```css
.panel {
    background-color: rgb(24, 49, 83);
}
```

Los canales se expresan normalmente entre 0 y 255. La notación moderna también admite porcentajes.

La transparencia puede expresarse mediante el canal alfa:

```css
.sombra {
    background-color: rgb(0 0 0 / 20%);
}
```

El canal alfa no cambia el color de los canales RGB: determina cuánto se compone con lo que hay detrás.

## 5. HSL

HSL describe el color mediante:
- **Hue (matiz):** posición en el círculo cromático, expresada en grados.
- **Saturation (saturación):** intensidad del color, en porcentaje.
- **Lightness (luminosidad):** claridad, en porcentaje.

```css
.boton {
    background-color: hsl(210 60% 35%);
}
```

HSL puede resultar intuitivo para generar variaciones de un color: se mantiene el matiz y se modifica la luminosidad o saturación.

## 6. Propiedades de color

```css
body {
    color: #263238;
    background-color: #f5f7fa;
}

button {
    color: white;
    background-color: #174a6e;
    border-color: #174a6e;
}
```

- `color`: color del texto y, por herencia, de otros contenidos textuales.
- `background-color`: color de fondo del área de un elemento.
- `border-color`: color del borde.

Un fondo transparente permite ver el fondo que hay detrás.

## 7. Contraste y uso responsable

Un texto debe distinguirse claramente del fondo. La combinación debe comprobarse, especialmente para texto pequeño y estados de interfaz. No basta con que dos colores sean diferentes: importa la diferencia de luminancia y cómo se perciben.

No se debe transmitir «correcto» únicamente en verde y «error» únicamente en rojo. Añade etiquetas, iconos o mensajes.

## 8. Ejemplo guiado: paleta coherente

```css
:root {
    --color-principal: #174a6e;
    --color-texto: #263238;
    --color-fondo: #f5f7fa;
    --color-aviso: #fff3cd;
}

body {
    color: var(--color-texto);
    background-color: var(--color-fondo);
}

h1 {
    color: var(--color-principal);
}

.aviso {
    background-color: var(--color-aviso);
}
```

Las variables CSS permiten centralizar valores reutilizados. Se introducen aquí como recurso práctico para evitar repetir códigos de color; el estudio más amplio de variables y arquitectura de CSS puede ampliarse posteriormente.

## 9. Errores frecuentes

- Escribir un hexadecimal con caracteres no válidos.
- Confundir transparencia con luminosidad.
- Elegir colores sin comprobar contraste.
- Utilizar demasiados colores sin una función definida.
- Comunicar estados únicamente mediante color.

## 10. Actividades

**E23. Lectura.** Descompón `#2A5B8A` en sus tres canales RGB.

**E24. Equivalencia.** Expresa un color en hexadecimal y RGB. Comprueba visualmente que representan el mismo color.

**E25. Variaciones.** Utiliza HSL para crear tres variantes de un mismo matiz con distinta luminosidad.

**E26. Auditoría.** Revisa una interfaz con texto gris claro sobre fondo blanco y propone mejoras.

## 11. Reto práctico

Define una paleta para una web educativa con color principal, secundario, fondo, texto y aviso. Documenta la función de cada color y comprueba el contraste de las combinaciones de texto.

## 12. Comprobación final

- [ ] Interpreto la notación hexadecimal.
- [ ] Distingo RGB de HSL.
- [ ] Comprendo el canal alfa.
- [ ] Selecciono colores con una función y contraste adecuados.
