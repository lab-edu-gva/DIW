# S12 · Posicionamiento absolute, fixed y sticky

---
asignatura: DIW
unidad: UD3
sesion: 12
tipo: material-alumnado
estado: preparado
publicar: true
---

## 1. Tres comportamientos distintos

`absolute`, `fixed` y `sticky` permiten resolver necesidades diferentes. La diferencia principal está en la referencia de posicionamiento y en cómo participa el elemento en el flujo.

## 2. `position: absolute`

Un elemento absoluto sale del flujo normal: no reserva su espacio original. Sus offsets se calculan respecto a su bloque contenedor de referencia, que normalmente será el ancestro posicionado más cercano.

```css
.tarjeta {
    position: relative;
}

.etiqueta {
    position: absolute;
    top: 0.5rem;
    right: 0.5rem;
}
```

HTML:

```html
<article class="tarjeta">
    <span class="etiqueta">Nuevo</span>
    <h2>Curso de CSS</h2>
    <p>Aprende a diseñar interfaces.</p>
</article>
```

La tarjeta establece el contexto con `relative`; la etiqueta se sitúa en su esquina superior derecha.

Si no existe un ancestro adecuado, el elemento puede posicionarse respecto a otro bloque de referencia, con resultados inesperados. Por eso se suele preparar el contenedor explícitamente.

## 3. `position: fixed`

Un elemento fijo se posiciona respecto al viewport en los casos habituales y permanece en la misma posición visible durante el desplazamiento:

```css
.boton-ayuda {
    position: fixed;
    right: 1rem;
    bottom: 1rem;
}
```

Puede utilizarse para un botón de ayuda persistente, pero debe comprobarse que no tapa contenido ni controles, especialmente en móviles y con zoom.

Ciertos ancestros con propiedades como `transform` pueden alterar el bloque de referencia de un descendiente fijo; no conviene asumir que siempre se comportará respecto al viewport en cualquier estructura.

## 4. `position: sticky`

Un elemento sticky se comporta como relativo hasta alcanzar un umbral de desplazamiento y, entonces, queda adherido dentro de los límites de su contenedor:

```css
.cabecera-seccion {
    position: sticky;
    top: 0;
}
```

Es habitual en cabeceras o títulos de sección. Necesita un umbral como `top` para saber cuándo adherirse y puede verse afectado por los contenedores de desplazamiento y la estructura de ancestros.

## 5. Comparación

| Valor | Participa en el flujo | Referencia habitual |
|---|---|---|
| `absolute` | No | Ancestro de referencia |
| `fixed` | No | Viewport, salvo contextos especiales |
| `sticky` | Sí, conserva su espacio | Contenedor de desplazamiento |

## 6. Ejemplo guiado: tarjeta con etiqueta

```css
.tarjeta {
    position: relative;
    padding: 2rem 1rem 1rem;
    border: 1px solid #cbd5e1;
}

.etiqueta {
    position: absolute;
    top: 0;
    right: 0;
    padding: 0.25rem 0.6rem;
    background: #174a6e;
    color: white;
}
```

La etiqueta queda anclada a la tarjeta y no empuja el título ni el párrafo. El padding superior evita que el contenido se solape visualmente con ella.

## 7. Capas y `z-index`

Cuando cajas posicionadas se solapan, `z-index` puede controlar su orden de apilamiento en los contextos donde resulta aplicable:

```css
.modal {
    position: fixed;
    z-index: 1000;
}
```

Un número mayor no garantiza estar por encima de cualquier elemento de la página: los contextos de apilamiento pueden limitar la comparación. `z-index` no es una solución universal a cualquier solapamiento.

## 8. Errores frecuentes

- Olvidar `position:relative` en el contenedor de una etiqueta absoluta.
- Esperar que absolute reserve espacio.
- Colocar un botón fixed encima de contenido importante.
- Usar sticky sin `top`, `bottom` u otro umbral.
- Suponer que un `z-index` enorme siempre gana.

## 9. Actividades

**E46. Clasificación.** Identifica qué posicionamiento utilizarías para una etiqueta de tarjeta, un botón flotante y un encabezado que se adhiere al desplazarse.

**E47. Implementación.** Crea una tarjeta con etiqueta absoluta y contenedor relativo.

**E48. Experimentación.** Añade un botón fixed y comprueba su comportamiento al desplazar la página y cambiar el tamaño de ventana.

**E49. Diagnóstico.** Un elemento sticky no se adhiere. Comprueba umbral, contenedores y estructura.

**E50. Capas.** Crea dos elementos solapados y experimenta con `z-index`. Explica qué ocurre si pertenecen a contextos de apilamiento diferentes.

## 10. Reto práctico

Construye una página de artículo con cabecera sticky, una etiqueta absoluta dentro de una tarjeta y un botón de ayuda fixed. Verifica que ninguno tapa contenido ni impide interactuar con la página.

## 11. Comprobación final

- [ ] Distingo absolute, fixed y sticky.
- [ ] Identifico la referencia de un elemento absoluto.
- [ ] Sé por qué fixed puede tapar contenido.
- [ ] Comprendo el papel de z-index y los contextos de apilamiento.
