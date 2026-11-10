# S10 · Desbordamiento: overflow

---
asignatura: DIW
unidad: UD3
sesion: 10
tipo: material-alumnado
estado: preparado
publicar: true
---

## 1. ¿Qué ocurre cuando el contenido no cabe?

Una caja puede tener dimensiones limitadas y recibir contenido que supera el espacio disponible. Ese fenómeno se denomina desbordamiento (*overflow*).

Puede ocurrir con texto largo, imágenes, tablas, código o elementos hijos. La solución correcta depende del contenido y de la experiencia que se quiera ofrecer.

## 2. `overflow`

La propiedad controla cómo se presenta el contenido que excede la caja:

```css
.contenedor {
    width: 300px;
    height: 120px;
    overflow: auto;
}
```

Valores principales:
- `visible`: el contenido puede sobresalir; es el comportamiento inicial habitual.
- `hidden`: recorta el contenido que desborda y no muestra barras de desplazamiento.
- `scroll`: proporciona mecanismos de desplazamiento, incluso cuando no siempre hacen falta.
- `auto`: permite desplazamiento cuando es necesario.

## 3. Ejes independientes

Se puede controlar cada eje:

```css
.panel {
    overflow-x: auto;
    overflow-y: hidden;
}
```

Esto es útil, por ejemplo, para una tabla ancha que necesita desplazamiento horizontal. Sin embargo, no debe utilizarse como excusa para no adaptar una tabla o un contenido a pantallas pequeñas.

## 4. Texto y contenido no divisible

Una cadena muy larga puede romper el diseño:

```css
.codigo {
    overflow-wrap: anywhere;
}
```

La propiedad permite establecer oportunidades de salto para evitar que una palabra o cadena desborde el contenedor.

En imágenes también conviene controlar dimensiones:

```css
img {
    max-width: 100%;
    height: auto;
}
```

## 5. Ejemplo guiado

HTML:

```html
<div class="panel">
    <p>Contenido de ejemplo repetido para provocar un desbordamiento y observar el comportamiento del contenedor.</p>
</div>
```

CSS:

```css
.panel {
    width: 260px;
    height: 100px;
    border: 1px solid #174a6e;
    overflow: auto;
}
```

Prueba a sustituir `auto` por `visible`, `hidden` y `scroll`. Observa qué parte del contenido queda accesible y qué experiencia obtiene la persona usuaria.

## 6. Precauciones de diseño

- No ocultes contenido esencial sin proporcionar otra forma de acceder a él.
- No fijes alturas pequeñas para textos que pueden variar.
- Comprueba tablas, código y textos largos.
- Comprueba el comportamiento con zoom y tamaños de pantalla distintos.
- Utiliza desplazamiento en un componente solo cuando sea comprensible y controlable.

## 7. Errores frecuentes

- Utilizar `hidden` para ocultar un fallo de dimensiones.
- Cortar texto esencial.
- Olvidar el eje horizontal en tablas anchas.
- Fijar altura sin considerar el crecimiento del contenido.
- Confundir overflow con `display:none`.

## 8. Actividades

**E39. Experimentación.** Construye una caja con texto largo y prueba `visible`, `hidden`, `scroll` y `auto`.

**E40. Diagnóstico.** Una tabla provoca desplazamiento horizontal en toda la página. Propón una solución localizada y explica sus límites.

**E41. Texto largo.** Evita que una cadena sin espacios rompa una tarjeta.

**E42. Revisión.** Identifica qué información quedaría inaccesible si se aplica `overflow:hidden` a un contenedor de altura fija.

## 9. Reto práctico

Construye un panel de actividad con altura limitada y desplazamiento interno. Debe quedar claro visualmente que existe más contenido y debe poder recorrerse con teclado y ratón.

## 10. Comprobación final

- [ ] Explico qué es el desbordamiento.
- [ ] Distingo los valores principales de overflow.
- [ ] Sé controlar los ejes.
- [ ] Evito recortar información importante.
