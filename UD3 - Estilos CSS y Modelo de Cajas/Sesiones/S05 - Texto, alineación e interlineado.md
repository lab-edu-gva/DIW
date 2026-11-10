# S05 · Texto, alineación e interlineado

---
asignatura: DIW
unidad: UD3
sesion: 5
tipo: material-alumnado
estado: preparado
publicar: true
---

## 1. Legibilidad frente a decoración

El texto de una interfaz se consume en condiciones muy distintas: monitores grandes, portátiles, móviles, diferentes distancias de lectura y preferencias de usuario. El objetivo no es decorar cada párrafo, sino facilitar que el contenido se comprenda.

## 2. Alineación: `text-align`

```css
h1 {
    text-align: center;
}

p {
    text-align: left;
}
```

Valores frecuentes:
- `left`: alineación izquierda.
- `right`: alineación derecha.
- `center`: centrado.
- `justify`: ajusta el texto a ambos márgenes.

El texto centrado funciona bien en títulos breves, pero dificulta seguir líneas largas. La justificación puede generar espacios irregulares, especialmente en columnas estrechas.

## 3. Interlineado: `line-height`

Controla la altura de línea:

```css
p {
    font-size: 1rem;
    line-height: 1.6;
}
```

Un valor sin unidad funciona como factor multiplicador del tamaño de fuente. En el ejemplo, la altura de línea es aproximadamente 1,6 veces el tamaño del texto.

Un interlineado demasiado pequeño hace que las líneas parezcan amontonadas. Uno excesivo rompe la continuidad visual.

## 4. Espaciado entre letras y palabras

```css
h1 {
    letter-spacing: 0.03em;
}

p {
    word-spacing: 0.05em;
}
```

- `letter-spacing`: modifica el espacio entre caracteres.
- `word-spacing`: modifica el espacio entre palabras.

Son propiedades para ajustes puntuales. Aumentar mucho el espaciado puede perjudicar el reconocimiento de palabras.

## 5. Transformación y decoración del texto

```css
.etiqueta {
    text-transform: uppercase;
}

a {
    text-decoration: none;
}
```

`text-transform` cambia la presentación de mayúsculas/minúsculas sin modificar el texto original. `text-decoration` controla decoraciones como subrayado o tachado.

No se debe eliminar el subrayado de los enlaces sin ofrecer otra señal visual clara que permita reconocerlos como enlaces.

## 6. Sangría y control de líneas

```css
p {
    text-indent: 1.5em;
}
```

`text-indent` establece la sangría de la primera línea de un bloque de texto.

Para controlar cómo se comporta el texto largo pueden utilizarse propiedades como `overflow-wrap`, que ayuda a evitar desbordamientos de cadenas largas:

```css
.codigo {
    overflow-wrap: anywhere;
}
```

La propiedad no sustituye a un diseño correcto de columnas y anchos.

## 7. Ejemplo guiado: artículo legible

```css
.articulo {
    max-width: 70ch;
    margin: 0 auto;
    font-family: Georgia, serif;
    font-size: 1.05rem;
    line-height: 1.65;
    color: #30343b;
}

.articulo h1 {
    font-family: Arial, sans-serif;
    line-height: 1.2;
    text-align: left;
}

.articulo p {
    text-align: left;
}
```

`max-width: 70ch` limita la longitud de línea utilizando el ancho aproximado del carácter `0` de la fuente. Es una técnica útil para evitar líneas excesivamente largas.

## 8. Errores frecuentes

- Centrar todos los párrafos por estética.
- Utilizar `line-height` demasiado reducido.
- Separar letras de forma exagerada.
- Eliminar la decoración de enlaces sin alternativa.
- Confundir `text-align` con la alineación de un contenedor Flexbox.

## 9. Actividades

**E19. Comparación.** Crea tres párrafos con alineación izquierda, centrada y justificada. Explica cuál se lee mejor en una columna estrecha.

**E20. Interlineado.** Compara `line-height: 1`, `1.5` y `2`. Describe el efecto.

**E21. Ajuste.** Diseña un artículo con ancho máximo, interlineado y jerarquía de títulos coherentes.

**E22. Accesibilidad básica.** Revisa enlaces cuyo subrayado se ha eliminado y propón una alternativa visual reconocible.

## 10. Reto práctico

Maqueta un artículo de lectura larga con título, subtítulo, varios párrafos, una cita y enlaces. Prioriza la lectura cómoda frente a los efectos decorativos.

## 11. Comprobación final

- [ ] Configuro alineación e interlineado.
- [ ] Distingo espaciado entre letras y palabras.
- [ ] Comprendo el efecto de `max-width` y `ch`.
- [ ] Evito decisiones que reduzcan la legibilidad.
