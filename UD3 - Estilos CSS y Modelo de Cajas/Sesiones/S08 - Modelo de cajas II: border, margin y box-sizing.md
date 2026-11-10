# S08 · Modelo de cajas II: border, margin y box-sizing

---
asignatura: DIW
unidad: UD3
sesion: 8
tipo: material-alumnado
estado: preparado
publicar: true
---

## 1. Border: el límite visible de la caja

El borde rodea el contenido y el padding. Para definirlo se suelen especificar grosor, estilo y color:

```css
.tarjeta {
    border-width: 1px;
    border-style: solid;
    border-color: #cbd5e1;
}
```

Forma abreviada:

```css
.tarjeta {
    border: 1px solid #cbd5e1;
}
```

El estilo es importante: si no se define un estilo visible, el borde puede no mostrarse aunque tenga grosor y color.

## 2. Bordes por lado y esquinas

```css
.tarjeta {
    border-bottom: 3px solid #174a6e;
    border-radius: 12px;
}
```

`border-radius` redondea las esquinas. Puede utilizarse para suavizar componentes, pero no sustituye a una estructura clara ni debe aplicarse sin criterio a todos los elementos.

## 3. Margin: espacio exterior

El margen separa la caja de los elementos vecinos:

```css
.tarjeta {
    margin: 16px;
}
```

A diferencia del padding, el margen está fuera del borde y el fondo del elemento no se pinta en esa zona.

Puede configurarse por lados y con abreviaturas. Un uso frecuente es centrar horizontalmente un bloque con anchura limitada:

```css
.contenedor {
    width: 800px;
    margin-left: auto;
    margin-right: auto;
}
```

En diseños fluidos, normalmente se combina `max-width` con márgenes automáticos.

## 4. Colapso de márgenes

En determinados contextos de flujo de bloques, los márgenes verticales pueden colapsar: dos márgenes adyacentes no siempre se suman, sino que puede prevalecer el mayor de los dos (considerando también márgenes negativos).

Este comportamiento puede sorprender cuando se espera una suma aritmética. No se produce de la misma forma con márgenes horizontales ni en todos los contextos de formato.

Para esta unidad basta con reconocer el fenómeno y aprender a inspeccionarlo; no conviene solucionarlo añadiendo márgenes arbitrarios.

## 5. `box-sizing`: cómo se calcula el tamaño

Con `content-box`, `width` y `height` definen el contenido. Padding y borde se añaden.

Con `border-box`, las dimensiones declaradas incluyen contenido, padding y borde:

```css
* {
    box-sizing: border-box;
}
```

Este patrón hace más predecible el cálculo de anchuras y ya se ha trabajado anteriormente; aquí se relaciona con el modelo completo.

### Cálculo comparado

Supongamos:
- `width: 300px`
- `padding: 20px` a izquierda y derecha
- `border: 5px` a izquierda y derecha

Con `content-box`:
300 + 40 + 10 = **350 px** de ancho total.

Con `border-box`:
**300 px** de ancho total; el contenido disponible se reduce para dejar espacio al padding y al borde.

## 6. Patrón de proyecto

```css
*,
*::before,
*::after {
    box-sizing: border-box;
}

.contenedor {
    width: min(100% - 2rem, 70rem);
    margin-inline: auto;
}

.tarjeta {
    padding: 1.25rem;
    border: 1px solid #cbd5e1;
    border-radius: 0.75rem;
}
```

El selector universal y los pseudoelementos se utilizan para que el cálculo sea coherente en los elementos y sus cajas generadas. La sintaxis de `min()` y `margin-inline` se presenta como ampliación práctica.

## 7. Diferencias esenciales

| Propiedad | Zona | ¿Se pinta el fondo detrás? |
|---|---|---|
| `padding` | Entre contenido y borde | Sí |
| `border` | Límite de la caja | El fondo llega hasta el borde según `background-clip` |
| `margin` | Fuera del borde | No |

## 8. Errores frecuentes

- Utilizar margin cuando se necesita espacio interior.
- Olvidar `border-style`.
- Calcular dimensiones sin tener en cuenta el modelo de caja.
- Suponer que los márgenes verticales siempre se suman.
- Aplicar `box-sizing` solo a unos pocos elementos sin una razón clara.

## 9. Actividades

**E31. Cálculo.** Calcula el ancho total de una caja de 240 px con 15 px de padding y 2 px de borde a cada lado en `content-box`.

**E32. Comparación.** Repite el cálculo con `border-box` y explica qué dimensión permanece constante.

**E33. Maquetación.** Diseña una tarjeta con borde, esquinas redondeadas, padding y margen exterior.

**E34. Diagnóstico.** Corrige un contenedor que supera el ancho disponible debido a padding y bordes.

## 10. Reto práctico

Construye una cuadrícula de tres tarjetas con ancho coherente, separación exterior y espacio interior. Usa `border-box` y explica por qué simplifica el cálculo.

## 11. Comprobación final

- [ ] Distingo borde y margen.
- [ ] Calculo dimensiones con `content-box` y `border-box`.
- [ ] Comprendo el colapso vertical de márgenes.
- [ ] Utilizo el modelo de caja de forma consistente.
