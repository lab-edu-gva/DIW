# S11 · Posicionamiento CSS: static y relative

---
asignatura: DIW
unidad: UD3
sesion: 11
tipo: material-alumnado
estado: preparado
publicar: true
---

## 1. Flujo normal y posicionamiento

Por defecto, los elementos se colocan siguiendo el flujo normal del documento. Los bloques suelen apilarse y el contenido en línea fluye dentro de las líneas.

La propiedad `position` permite modificar cómo se sitúa una caja. Es importante entender que posicionar no equivale a «mover algo hasta que quede bonito»: cada modo tiene reglas sobre el espacio que conserva y el contexto respecto al que se calcula.

## 2. `position: static`

Es el valor inicial habitual. El elemento permanece en el flujo normal y las propiedades `top`, `right`, `bottom` y `left` no desplazan su caja.

```css
.elemento {
    position: static;
}
```

No es necesario declarar `static` salvo para restablecer explícitamente otro posicionamiento.

## 3. `position: relative`

El elemento se mantiene en el flujo normal, pero puede desplazarse respecto a su posición original:

```css
.elemento {
    position: relative;
    top: 10px;
    left: 15px;
}
```

La caja se dibuja desplazada, pero conserva el espacio que ocupaba originalmente. Por eso puede aparecer un hueco en su posición inicial.

## 4. Crear un contexto para descendientes posicionados

Un uso muy habitual de `relative` es establecer un bloque de referencia para un descendiente con `position:absolute`:

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

En esta sesión solo se introduce el motivo de utilizarlo; el posicionamiento absoluto se desarrolla en la siguiente.

## 5. Ejemplo guiado: desplazamiento relativo

```html
<div class="caja">Caja original</div>
<p>Texto posterior</p>
```

```css
.caja {
    width: 180px;
    padding: 1rem;
    background: #dcecf7;
    position: relative;
    left: 30px;
    top: 10px;
}
```

La caja se representa desplazada 30 píxeles a la derecha y 10 hacia abajo. El párrafo posterior conserva el lugar que le corresponde en el flujo original.

## 6. Cuándo utilizarlo

- `static`: comportamiento normal.
- `relative`: desplazamiento pequeño respecto a la posición original o creación de referencia para descendientes absolutos.

No utilices `relative` como sustituto de Flexbox o Grid para construir una maquetación completa. Para distribuir columnas, filas y espacios, los sistemas de layout son más robustos.

## 7. Errores frecuentes

- Esperar que `top` funcione con `position:static`.
- Creer que `relative` elimina el espacio original.
- Mover muchos elementos con offsets para construir toda una página.
- No comprender respecto a qué referencia se desplaza la caja.

## 8. Actividades

**E43. Predicción.** Explica qué sucede al aplicar `top:20px` a un elemento estático y a uno relativo.

**E44. Experimentación.** Desplaza una caja con `relative` y observa el espacio que sigue reservando.

**E45. Decisión.** Elige entre flujo normal, Flexbox/Grid o posicionamiento relativo para tres escenarios y justifica.

## 9. Reto práctico

Construye una tarjeta cuyo elemento principal permanezca en el flujo normal y cuya caja se desplace ligeramente para ilustrar `relative`. Documenta por qué no usarías offsets para maquetar toda la interfaz.

## 10. Comprobación final

- [ ] Explico el flujo normal.
- [ ] Distingo static y relative.
- [ ] Comprendo que relative conserva el espacio original.
- [ ] Identifico un uso razonable de relative.
