# S03 · Cascada, herencia y especificidad

---
asignatura: DIW
unidad: UD3
sesion: 3
tipo: material-alumnado
estado: preparado
publicar: true
---

## 1. ¿Qué ocurre cuando varias reglas afectan al mismo elemento?

CSS significa *Cascading Style Sheets*: hojas de estilo en cascada. La cascada es el mecanismo que permite decidir qué declaración prevalece cuando varias podrían aplicarse a un mismo elemento.

No es correcto pensar que siempre gana la última regla. La decisión depende de varios factores, entre ellos el origen e importancia de la declaración, la especificidad del selector y el orden cuando los demás factores relevantes empatan.

## 2. El orden de las reglas

Cuando dos declaraciones tienen la misma importancia y la misma especificidad, prevalece la que aparece después:

```css
p {
    color: navy;
}

p {
    color: darkgreen;
}
```

El texto será verde oscuro. La segunda regla no gana por estar «más abajo» en cualquier circunstancia, sino porque en este caso existe un empate en los factores anteriores.

## 3. Especificidad: no todos los selectores pesan igual

Como aproximación didáctica, podemos comparar:
- Identificadores: mayor peso.
- Clases, atributos y pseudoclases: peso intermedio.
- Elementos y pseudoelementos: menor peso.

Ejemplo:

```css
p {
    color: black;
}

.texto {
    color: blue;
}

#principal {
    color: red;
}
```

HTML:

```html
<p id="principal" class="texto">Contenido</p>
```

Las tres reglas coinciden, pero el selector de identificador tiene mayor especificidad que la clase y el selector de tipo. El texto se muestra rojo.

La especificidad no es una competición de cantidad de caracteres. Se calcula mediante categorías de selectores; no conviene resolver conflictos añadiendo identificadores de forma indiscriminada.

## 4. Herencia

Algunas propiedades se transmiten desde un elemento antecesor a sus descendientes. Es habitual en propiedades relacionadas con el texto, como `color` y `font-family`.

```css
body {
    color: #333333;
    font-family: Arial, sans-serif;
}
```

Los elementos descendientes suelen heredar esos valores si no tienen una declaración propia que los sustituya.

No todas las propiedades se heredan. Por ejemplo, `margin`, `padding` y `border` no se transmiten automáticamente a los hijos.

## 5. Valores especiales: `inherit`, `initial` y `unset`

- `inherit`: fuerza a tomar el valor calculado del elemento padre.
- `initial`: establece el valor inicial definido por CSS para esa propiedad.
- `unset`: se comporta como `inherit` si la propiedad se hereda normalmente y como `initial` si no.

Ejemplo:

```css
article {
    color: darkslategray;
}

article strong {
    color: inherit;
}
```

El texto resaltado hereda explícitamente el color del artículo.

## 6. `!important`: una herramienta excepcional

```css
p {
    color: red !important;
}
```

`!important` altera la prioridad de la declaración dentro de las reglas de cascada. No debe utilizarse para «arreglar» cualquier conflicto: puede dificultar el mantenimiento y provocar una cadena de reglas cada vez más difíciles de sobrescribir.

La solución profesional suele ser revisar el selector, el orden y la organización de la hoja de estilos.

## 7. Método de diagnóstico

Cuando un estilo no produce el resultado esperado:

1. Comprueba que el archivo CSS se ha cargado.
2. Inspecciona el elemento y confirma qué selectores coinciden.
3. Localiza las declaraciones que afectan a la propiedad.
4. Comprueba si alguna está tachada por otra regla.
5. Compara importancia y especificidad.
6. Revisa el orden cuando exista empate.
7. Comprueba si el valor procede de herencia.

Las herramientas de desarrollador del navegador permiten inspeccionar reglas aplicadas y valores calculados.

## 8. Ejemplo guiado

```html
<section class="panel">
    <p id="mensaje" class="aviso">Revisa tu solicitud.</p>
</section>
```

```css
.panel {
    color: #333333;
}

p {
    color: navy;
}

.aviso {
    color: darkgreen;
}

#mensaje {
    color: maroon;
}

.panel p {
    font-size: 1.1rem;
}
```

El párrafo recibe `font-size` de `.panel p`. En cuanto a `color`, coincide con `p`, `.aviso` y `#mensaje`; el identificador tiene mayor especificidad. El color final es granate.

Si eliminamos la regla `#mensaje`, gana `.aviso` frente a `p`.

## 9. Errores frecuentes

- Creer que la última regla siempre gana.
- Confundir herencia con aplicación directa de una regla.
- Suponer que todas las propiedades se heredan.
- Añadir `!important` sin comprender el conflicto.
- No inspeccionar el elemento en el navegador.

## 10. Actividades

**E11. Predicción.** Determina el color final de un párrafo al que afectan una regla de tipo, una clase y un identificador.

**E12. Herencia.** Indica cuáles de estas propiedades se heredan normalmente: `color`, `font-family`, `margin`, `border`, `line-height`.

**E13. Diagnóstico.** Se proporciona una hoja con reglas contradictorias. Explica qué regla gana y por qué.

**E14. Refactorización.** Elimina usos innecesarios de `!important` reorganizando selectores y declaraciones.

## 11. Reto práctico

Diseña una tarjeta que herede tipografía y color general de `body`, pero tenga un título y un aviso con estilos propios. Incluye dos reglas en conflicto y documenta por escrito cómo se resuelve la cascada.

## 12. Comprobación final

- [ ] Explico qué es la cascada.
- [ ] Comparo la especificidad de selectores básicos.
- [ ] Distingo herencia y aplicación directa.
- [ ] Sé diagnosticar conflictos con las herramientas del navegador.
