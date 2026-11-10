---
asignatura: DIW
unidad: UD2
sesion: 05
tipo: material-alumnado
estado: preparado
programacion: "UP2 - Estructura HTML y Semántica HTML5"
duracion: "55 minutos"
---

# Sesión 05 · Secciones y contenido independiente: section, article y aside

> [!abstract] Propósito de la sesión
> Diferenciar agrupaciones temáticas, contenidos autónomos e información complementaria.

## Objetivos de aprendizaje
- Elegir entre `section`, `article` y `aside`.
- Combinar elementos semánticos dentro de `main`.
- Organizar contenidos complejos con encabezados adecuados.

## Desarrollo de contenidos

## 1. `section`: agrupación temática

`<section>` representa una sección temática de un documento. Normalmente tiene un encabezado que anuncia el tema tratado.

```html
<section>
    <h2>Próximos eventos</h2>
    <p>Consulta las actividades del centro.</p>
</section>
```

No debe utilizarse como contenedor genérico por defecto. Si solo necesitamos agrupar elementos sin significado semántico adicional, un contenedor genérico puede ser más apropiado.

## 2. `article`: contenido autónomo

`<article>` representa una composición que puede tener sentido por sí misma y ser distribuida o reutilizada de forma independiente: una noticia, una entrada, una publicación o una ficha autónoma.

```html
<article>
    <h2>Jornada de puertas abiertas</h2>
    <p>El centro celebrará una jornada informativa...</p>
</article>
```

Un artículo puede incluir su propia cabecera y pie si el contenido lo requiere.

## 3. `aside`: contenido complementario

`<aside>` contiene información relacionada de forma indirecta con el contenido principal: recomendaciones, glosarios, notas laterales o enlaces complementarios.

```html
<aside>
    <h2>Información relacionada</h2>
    <p>La inscripción se realiza en secretaría.</p>
</aside>
```

No significa necesariamente “columna derecha”. La ubicación visual se decidirá con CSS.

## 4. Cómo decidir

Pregúntate:

1. ¿Es un contenido autónomo que podría publicarse por separado? Puede ser `article`.
2. ¿Es una parte temática de un documento mayor? Puede ser `section`.
3. ¿Es información complementaria al contenido principal? Puede ser `aside`.
4. ¿Solo necesito agrupar elementos sin aportar significado? Un contenedor genérico puede ser suficiente.

## 5. Ejemplo combinado

```html
<main>
    <section>
        <h2>Noticias del centro</h2>
        <article>
            <h3>Nuevo laboratorio</h3>
            <p>El centro estrena un espacio de prácticas.</p>
        </article>
        <article>
            <h3>Concurso de programación</h3>
            <p>La inscripción estará abierta hasta el viernes.</p>
        </article>
    </section>

    <aside>
        <h2>Enlaces de interés</h2>
        <p>Consulta el calendario académico.</p>
    </aside>
</main>
```

## 6. Errores habituales

- Usar `section` como sustituto universal de `div`.
- Crear un `article` para cualquier párrafo aislado.
- Elegir `aside` porque se quiere colocar una columna lateral.
- Saltar niveles de encabezado sin una razón estructural.

## Ejemplo guiado

### Ejemplo guiado: portal de noticias

Dentro de `main`, crea una sección “Noticias”. Añade dos artículos independientes y un bloque `aside` con información complementaria. Cada bloque debe tener un encabezado que describa su contenido.

## Actividades prácticas

### E17 · Clasificación semántica

Clasifica diez fragmentos: noticia, comentario, bloque temático, glosario, ficha de producto, recomendación y otros. Elige `section`, `article`, `aside` o contenedor genérico y justifica.

### E18 · Reestructurar un portal

Convierte una página con contenedores genéricos en una estructura semántica con `section`, `article` y `aside`.

### E19 · Jerarquía de contenidos

Crea una página de noticias con una sección, tres artículos y un bloque complementario. Organiza los encabezados sin saltos arbitrarios.

### E20 · Revisión por parejas

Intercambia el documento con un compañero. Comprueba si cada elemento semántico describe realmente el contenido que contiene.

## Reto de aplicación

Crea la estructura de una página de catálogo cultural con una sección de actividades, tres artículos independientes y un aside con información práctica. Explica por qué has elegido cada elemento.

## Errores que debes evitar

- Elegir etiquetas por su apariencia en lugar de por su significado.
- Escribir código sin revisar el anidamiento.
- Olvidar las etiquetas asociadas a los controles de formulario.
- Dar por válido un documento solo porque el navegador lo muestra.

## Resumen de la sesión

Al finalizar debes poder explicar los conceptos principales, construir un ejemplo pequeño y justificar las decisiones de marcado realizadas.

## Autoevaluación

- [ ] Sé distinguir `section` y `article`.
- [ ] Entiendo que `aside` expresa contenido complementario, no posición visual.
- [ ] Utilizo encabezados para identificar las secciones.
- [ ] Evito utilizar etiquetas semánticas como simples contenedores decorativos.

## Registro personal

- Dudas que me quedan:
- Errores que he corregido:
- Qué necesito practicar de nuevo:
