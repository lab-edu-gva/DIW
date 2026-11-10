# S09 · La propiedad display: block, inline e inline-block

---
asignatura: DIW
unidad: UD3
sesion: 9
tipo: material-alumnado
estado: preparado
publicar: true
---

## 1. El tipo de caja condiciona el flujo

La propiedad `display` determina cómo participa un elemento en el formato y distribución de la página. En esta sesión se estudian los valores fundamentales `block`, `inline`, `inline-block` y `none`.

No debe confundirse el elemento HTML con su presentación. Un mismo elemento puede cambiar su comportamiento visual mediante CSS sin que cambie su significado semántico.

## 2. `display: block`

Un elemento de bloque:
- Inicia normalmente una nueva línea.
- Ocupa el espacio disponible en la dirección horizontal si su anchura es automática.
- Admite dimensiones y modelo de caja de forma habitual.

Ejemplos habituales de elementos que se presentan como bloque por defecto son `div`, `p`, `section` y `h1`.

```css
.bloque {
    display: block;
    width: 300px;
    padding: 1rem;
}
```

## 3. `display: inline`

Un elemento en línea participa en la línea de texto:
- No inicia una nueva línea por sí mismo.
- Ocupa el espacio necesario para su contenido.
- `width` y `height` no se aplican como en una caja de bloque.
- El comportamiento vertical de padding y border tiene particularidades.

Ejemplos habituales: `span`, `a` y `strong`.

```css
.resaltado {
    display: inline;
    color: crimson;
}
```

## 4. `display: inline-block`

Combina características:
- Se coloca en línea con otros elementos.
- Admite anchura y altura.
- Respeta padding y borde como caja.

```css
.etiqueta {
    display: inline-block;
    width: 120px;
    padding: 0.5rem;
}
```

Puede ser útil para etiquetas o pequeños controles que deben compartir línea y tener dimensiones controladas.

## 5. `display: none`

El elemento no genera caja en el diseño:

```css
.oculto {
    display: none;
}
```

No es lo mismo que hacerlo transparente: el elemento deja de participar en el layout. Si se necesita ocultar contenido por motivos de accesibilidad o interacción, hay que estudiar el objetivo concreto; `display:none` también suele retirar el contenido del árbol de accesibilidad.

## 6. Comparación práctica

```html
<p>Texto con <span class="inline">un fragmento</span> en línea.</p>

<div class="bloque">Elemento de bloque</div>

<span class="etiqueta">Etiqueta A</span>
<span class="etiqueta">Etiqueta B</span>
```

```css
.inline {
    display: inline;
    background: #fff3cd;
}

.bloque {
    display: block;
    background: #dcecf7;
    padding: 1rem;
}

.etiqueta {
    display: inline-block;
    width: 120px;
    padding: 0.5rem;
    background: #e4f2e8;
}
```

Observa cómo se colocan y qué dimensiones admite cada tipo.

## 7. Relación con Flexbox y Grid

Flexbox y Grid también son valores de `display` (`display: flex` y `display: grid`). Se han trabajado previamente y se profundizarán en la UD4. En esta unidad nos centramos en entender el comportamiento de bloque y en línea que sirve de base al flujo normal.

## 8. Errores frecuentes

- Esperar que un `span` se comporte como un bloque sin cambiar `display`.
- Intentar asignar `width` a un elemento inline ordinario.
- Creer que `display:none` equivale a `opacity:0`.
- Cambiar el `display` de un elemento semántico sin comprender el resultado visual.
- Utilizar `div` para todo en vez de elegir HTML según su significado.

## 9. Actividades

**E35. Clasificación.** Clasifica varios elementos HTML según su comportamiento visual habitual y comprueba que CSS puede modificarlo.

**E36. Experimentación.** Convierte un `span` en bloque y un `div` en inline. Describe los cambios.

**E37. Componentes.** Crea una fila de etiquetas con `inline-block`, anchura y padding.

**E38. Diagnóstico.** Una anchura no se aplica al elemento esperado. Investiga si su `display` explica el comportamiento.

## 10. Reto práctico

Construye una pequeña barra de enlaces con etiquetas en línea y un bloque de contenido independiente. No utilices Flexbox ni Grid: el objetivo es practicar el flujo básico.

## 11. Comprobación final

- [ ] Explico la diferencia entre block e inline.
- [ ] Sé cuándo puede resultar útil inline-block.
- [ ] Distingo `display:none` de transparencia.
- [ ] Relaciono display con el flujo normal.
