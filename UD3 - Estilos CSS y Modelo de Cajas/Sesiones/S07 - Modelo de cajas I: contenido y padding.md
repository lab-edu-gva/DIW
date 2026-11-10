# S07 · Modelo de cajas I: contenido y padding

---
asignatura: DIW
unidad: UD3
sesion: 7
tipo: material-alumnado
estado: preparado
publicar: true
---

## 1. Todo elemento visual ocupa una caja

El navegador representa los elementos de la página mediante cajas rectangulares. El modelo de cajas explica cómo se calcula el espacio que ocupa un elemento y cómo se relaciona con los elementos que lo rodean.

El modelo clásico contiene cuatro zonas, desde el interior hacia el exterior:
1. **Content:** contenido.
2. **Padding:** relleno interior.
3. **Border:** borde.
4. **Margin:** margen exterior.

Comprender estas zonas permite resolver problemas típicos: tarjetas demasiado grandes, elementos pegados al borde o separaciones inesperadas.

## 2. Content: el área de contenido

El contenido puede ser texto, una imagen u otros elementos. Las propiedades `width` y `height` permiten establecer dimensiones, aunque su significado exacto depende del modelo de caja aplicado.

```css
.tarjeta {
    width: 300px;
    height: 150px;
}
```

Con `content-box`, esas dimensiones se refieren al área de contenido, no al total de la caja.

No conviene fijar alturas rígidas para bloques de texto que puedan crecer. El contenido puede variar por idioma, tamaño de letra o dispositivo.

## 3. Padding: espacio interior

El padding crea espacio entre el contenido y el borde:

```css
.tarjeta {
    padding: 20px;
}
```

La tarjeta gana espacio interior. El fondo del elemento se pinta también bajo el padding.

Se pueden definir los cuatro lados:

```css
.tarjeta {
    padding-top: 10px;
    padding-right: 20px;
    padding-bottom: 10px;
    padding-left: 20px;
}
```

O utilizar la forma abreviada:

```css
.tarjeta {
    padding: 10px 20px;
}
```

Dos valores significan: primero arriba/abajo; segundo derecha/izquierda.

## 4. Abreviaturas de cuatro valores

```css
.caja {
    padding: 10px 20px 30px 40px;
}
```

El orden es horario, empezando arriba:
- arriba: 10 px
- derecha: 20 px
- abajo: 30 px
- izquierda: 40 px

Con tres valores, el segundo se aplica a ambos lados horizontales. Es importante leer las abreviaturas con precisión.

## 5. Unidades

Para padding se utilizan habitualmente `px`, `rem` o `em`. Una unidad relativa facilita adaptar el espacio a la escala tipográfica.

```css
.tarjeta {
    padding: 1.25rem;
}
```

No se debe escribir `padding: 20;`: una longitud necesita unidad, salvo el valor cero.

## 6. Ejemplo guiado

```html
<article class="tarjeta">
    <h2>Curso de desarrollo web</h2>
    <p>Aprende a construir interfaces.</p>
</article>
```

```css
.tarjeta {
    width: 320px;
    padding: 24px;
    background-color: #eef4f8;
}
```

Con el modelo `content-box`, el ancho total será 320 + 24 + 24 = 368 píxeles, sin contar el borde ni el margen. El padding se suma al ancho de contenido.

## 7. Inspección con herramientas del navegador

En las herramientas de desarrollo se puede inspeccionar una caja y visualizar las zonas de contenido, padding, borde y margen. Esta vista permite contrastar lo que se espera con lo que el navegador calcula.

Procedimiento:
1. Abrir la página.
2. Inspeccionar la tarjeta.
3. Localizar el diagrama del modelo de cajas.
4. Modificar temporalmente el padding.
5. Observar cómo cambia el espacio interior y el tamaño.

## 8. Errores frecuentes

- Confundir padding con margin.
- Creer que el padding está fuera del borde.
- Olvidar que con `content-box` se suma al ancho.
- Utilizar alturas rígidas para contenido variable.
- Escribir abreviaturas sin recordar su orden.

## 9. Actividades

**E27. Identificación.** Dibuja una caja y etiqueta contenido, padding, borde y margen.

**E28. Cálculo.** Una caja tiene 300 px de contenido y 20 px de padding a cada lado. Calcula el ancho exterior antes de borde y margen con `content-box`.

**E29. Código.** Crea una tarjeta y aplica padding distinto arriba/abajo y a los lados.

**E30. Diagnóstico.** Una tarjeta parece más ancha de lo esperado. Inspecciona el modelo de cajas y explica la causa.

## 10. Reto práctico

Construye tres tarjetas con el mismo contenido y distintos valores de padding. Compara la comodidad de lectura y el espacio que ocupa cada una.

## 11. Comprobación final

- [ ] Identifico las cuatro zonas del modelo de cajas.
- [ ] Distingo contenido y padding.
- [ ] Interpreto abreviaturas de uno, dos, tres y cuatro valores.
- [ ] Calculo el ancho resultante en `content-box`.
