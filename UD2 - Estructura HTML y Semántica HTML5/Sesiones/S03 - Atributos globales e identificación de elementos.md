---
asignatura: DIW
unidad: UD2
sesion: 03
tipo: material-alumnado
estado: preparado
programacion: "UP2 - Estructura HTML y Semántica HTML5"
duracion: "55 minutos"
---

# Sesión 03 · Atributos globales e identificación de elementos

> [!abstract] Propósito de la sesión
> Utilizar atributos HTML para identificar, describir y configurar elementos sin alterar su significado.

## Objetivos de aprendizaje
- Reconocer qué es un atributo y cómo se escribe.
- Aplicar atributos globales frecuentes.
- Diferenciar `id` y `class` y asignarlos de forma coherente.

## Desarrollo de contenidos

## 1. Anatomía de un atributo

Un atributo se escribe normalmente en la etiqueta de apertura, con la forma `nombre="valor"`:

```html
<p id="introduccion" class="destacado" lang="es">Texto introductorio.</p>
```

Los atributos aportan información al elemento. Algunos son globales, porque pueden utilizarse en muchos tipos de elementos; otros son específicos de determinadas etiquetas.

## 2. Atributos globales frecuentes

- `id`: identifica de forma única un elemento dentro del documento.
- `class`: asigna una o varias clases para agrupar elementos.
- `title`: proporciona información complementaria, normalmente mostrada como ayuda contextual por el navegador.
- `lang`: identifica el idioma del contenido.
- `hidden`: indica que el elemento no debe presentarse en la página.
- `tabindex`: participa en el orden de navegación mediante teclado; debe utilizarse con criterio.
- `contenteditable`: permite editar el contenido directamente en el navegador; no implica que los cambios se guarden en un servidor.

## 3. `id` frente a `class`

`id` debe ser único en el documento. Es apropiado para identificar un elemento concreto. `class` puede repetirse y permite agrupar elementos que comparten una característica.

```html
<h1 id="titulo-principal">Catálogo</h1>
<p class="aviso">Plazo de inscripción abierto.</p>
<p class="aviso">Plazas limitadas.</p>
```

No asignes el mismo `id` a varios elementos. Si necesitas marcar varios elementos de forma común, utiliza `class`.

## 4. Varios atributos en un elemento

Un elemento puede contener varios atributos, separados por espacios:

```html
<p id="aviso-legal" class="nota importante" lang="es" title="Información legal">
    Consulta las condiciones.
</p>
```

Una clase puede contener varios nombres separados por espacios. Cada nombre representa una clase independiente.

## 5. Atributos booleanos

Algunos atributos se activan por su presencia, no por un valor textual concreto. Por ejemplo, `hidden` o `required`:

```html
<input type="text" required>
```

Escribir `required="false"` no es la forma correcta de desactivarlo: en HTML la presencia del atributo booleano significa que está activado.

## 6. Buenas prácticas

- Utiliza identificadores descriptivos, sin espacios.
- No repitas valores de `id`.
- No abuses de `title` como sustituto de instrucciones visibles.
- No uses `tabindex` positivo para reorganizar toda la navegación sin necesidad.
- No confundas atributos con etiquetas: `id` no es un elemento HTML.

## Ejemplo guiado

### Ejemplo guiado: identificar una ficha

Crea tres artículos con una clase común `ficha`. Asigna a cada uno un `id` diferente. Añade `lang="es"` al documento y `title` a un elemento que necesite una aclaración. Comprueba que los `id` no se repiten.

## Actividades prácticas

### E09 · Clasificación de atributos

Clasifica `id`, `class`, `title`, `lang`, `hidden`, `required` y `type`: indica cuáles son globales, cuáles son específicos y si son booleanos.

### E10 · id o class

Para diez situaciones propuestas por el profesor, decide si necesitas `id`, `class` o ambos. Justifica cada elección.

### E11 · Ficha identificada

Crea cuatro fichas de cursos con una clase común y un identificador único por ficha. Incluye título, idioma y una nota complementaria.

### E12 · Auditoría de atributos

Revisa un documento con identificadores duplicados, clases mal escritas y un `required="false"`. Corrige y explica los problemas.

## Reto de aplicación

Construye un listado de seis actividades. Cada actividad debe compartir una clase común, tener un identificador único y marcarse con `lang` cuando el idioma del fragmento sea distinto al principal.

## Errores que debes evitar

- Elegir etiquetas por su apariencia en lugar de por su significado.
- Escribir código sin revisar el anidamiento.
- Olvidar las etiquetas asociadas a los controles de formulario.
- Dar por válido un documento solo porque el navegador lo muestra.

## Resumen de la sesión

Al finalizar debes poder explicar los conceptos principales, construir un ejemplo pequeño y justificar las decisiones de marcado realizadas.

## Autoevaluación

- [ ] Sé explicar la diferencia entre `id` y `class`.
- [ ] Puedo escribir varios atributos en una etiqueta.
- [ ] Reconozco los atributos booleanos.
- [ ] Evito duplicar identificadores.

## Registro personal

- Dudas que me quedan:
- Errores que he corregido:
- Qué necesito practicar de nuevo:
