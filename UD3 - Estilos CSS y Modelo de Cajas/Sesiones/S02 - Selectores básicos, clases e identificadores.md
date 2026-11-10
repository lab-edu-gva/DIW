# S02 · Selectores básicos, clases e identificadores

---
asignatura: DIW
unidad: UD3
sesion: 2
tipo: material-alumnado
estado: preparado
publicar: true
---

## 1. El selector: elegir antes de modificar

Una hoja CSS puede contener cientos de reglas. El selector determina qué elementos HTML recibirán cada conjunto de declaraciones. Elegir bien el selector evita repetir código y reduce efectos secundarios.

## 2. Selector de tipo

Selecciona todos los elementos de un tipo:

```css
p {
    color: #444444;
}

h1 {
    font-size: 2rem;
}
```

La regla `p` afecta a todos los párrafos coincidentes, no solo al primero.

## 3. Selector de clase

Una clase permite asignar una misma característica a varios elementos. En HTML se escribe con `class`; en CSS se identifica con un punto:

```html
<p class="destacado">Plazo de matrícula abierto.</p>
<div class="destacado">Consulta las fechas.</div>
```

```css
.destacado {
    background-color: #fff3cd;
    padding: 1rem;
}
```

Una clase puede reutilizarse en muchos elementos y un elemento puede tener varias clases:

```html
<article class="tarjeta destacada">...</article>
```

Las clases deben expresar una función o característica comprensible. Nombres como `rojo` describen un aspecto concreto; nombres como `aviso` expresan mejor el propósito y permiten cambiar el diseño sin renombrar el HTML.

## 4. Selector de identificador

El atributo `id` identifica un elemento concreto dentro del documento:

```html
<header id="cabecera-principal">...</header>
```

```css
#cabecera-principal {
    border-bottom: 2px solid #174a6e;
}
```

En CSS se utiliza `#`. Un mismo `id` no debe repetirse en la página. Para estilos reutilizables suele ser preferible una clase.

## 5. Selector universal

El asterisco selecciona todos los elementos:

```css
* {
    box-sizing: border-box;
}
```

Se usa con cuidado porque su alcance es muy amplio. En la unidad ya se ha trabajado `box-sizing`; aquí se utiliza para reconocer el selector que suele acompañar a una regla de normalización.

## 6. Agrupación de selectores

La coma permite aplicar una misma regla a varios selectores:

```css
h1,
h2,
h3 {
    color: #174a6e;
    font-family: Arial, sans-serif;
}
```

Es más claro que duplicar exactamente las mismas declaraciones.

## 7. Selectores combinados sencillos

El espacio selecciona descendientes, es decir, elementos que aparecen dentro de otro elemento:

```css
nav a {
    text-decoration: none;
}
```

La regla selecciona enlaces que se encuentran dentro de `nav`. No selecciona necesariamente todos los enlaces del documento.

El selector de hijo directo `>` se estudiará con mayor profundidad en la unidad de selectores avanzados. De momento, conviene reconocer que no significa lo mismo que un espacio.

## 8. Cómo elegir

| Necesidad | Selector habitual |
|---|---|
| Todos los párrafos | `p` |
| Varios elementos con el mismo propósito | `.aviso` |
| Un elemento único identificado | `#cabecera` |
| Varios tipos con reglas comunes | `h1, h2` |
| Enlaces que están dentro de navegación | `nav a` |

## 9. Ejemplo guiado

HTML:

```html
<header id="cabecera">
    <h1>Biblioteca Abierta</h1>
</header>

<main>
    <p class="introduccion">Lee, aprende y comparte.</p>
    <p>Consulta nuestro catálogo.</p>
    <p class="aviso">La sala cerrará a las 18:00.</p>
</main>
```

CSS:

```css
p {
    color: #333333;
}

.introduccion {
    font-size: 1.2rem;
}

.aviso {
    background-color: #fff3cd;
}

#cabecera {
    background-color: #e8f1f8;
}
```

Análisis:
1. Los tres párrafos reciben el color general.
2. Solo el párrafo con clase `introduccion` aumenta de tamaño.
3. Solo el párrafo con clase `aviso` recibe el fondo amarillo claro.
4. La cabecera se selecciona por su identificador.

Las reglas se pueden combinar: un elemento puede recibir simultáneamente reglas de tipo, clase e identificador.

## 10. Errores frecuentes

- Olvidar el punto de `.clase` o la almohadilla de `#id`.
- Escribir `class="aviso"` y seleccionar `#aviso`.
- Repetir el mismo `id` en varios elementos.
- Crear clases con nombres ambiguos como `.cosa1`.
- Suponer que `nav a` selecciona todos los enlaces de la página.

## 11. Actividades

**E06. Traducción.** Escribe selectores para todos los `h2`, todos los elementos `.producto`, el elemento `#pie` y los enlaces dentro de `nav`.

**E07. HTML.** Crea cuatro tarjetas. Todas tendrán la clase `tarjeta`; una tendrá además `destacada`.

**E08. CSS.** Define una regla común para todas las tarjetas y otra exclusiva para la destacada.

**E09. Refactorización.** Sustituye estilos repetidos por una clase reutilizable. Justifica por qué mejora el mantenimiento.

**E10. Diagnóstico.** Corrige un ejemplo en el que el HTML utiliza `class="principal"` pero el CSS contiene `#principal`.

## 12. Reto práctico

Crea una lista de noticias con una clase común para cada noticia, una clase adicional para las noticias destacadas y un identificador para la cabecera. Aplica reglas diferentes sin duplicar innecesariamente código.

## 13. Comprobación final

- [ ] Distingo selector de tipo, clase e identificador.
- [ ] Sé escribir el selector CSS correspondiente a un atributo HTML.
- [ ] Comprendo la reutilización de clases.
- [ ] Puedo agrupar selectores y seleccionar descendientes.
