# S01 · CSS y separación de estructura y presentación

---
asignatura: DIW
unidad: UD3
sesion: 1
tipo: material-alumnado
estado: preparado
publicar: true
---

## 1. ¿Qué problema resuelve CSS?

HTML describe la estructura y el significado del contenido; CSS determina cómo se presenta visualmente. Esta separación permite modificar la apariencia de un sitio sin tener que reescribir su contenido.

Imagina una web con veinte páginas. Si cada título contiene instrucciones visuales directamente en HTML, cambiar el color corporativo obliga a revisar veinte documentos. Si las reglas están centralizadas en una hoja CSS, basta con modificar una declaración.

La separación aporta:
- **Mantenimiento:** los cambios visuales se realizan en un lugar controlado.
- **Consistencia:** los componentes comparten reglas comunes.
- **Reutilización:** una misma hoja puede aplicarse a varias páginas.
- **Accesibilidad y semántica:** HTML conserva su función estructural y no se utiliza como mero mecanismo de decoración.

CSS no sustituye a HTML. Ambos lenguajes cooperan.

## 2. Anatomía de una regla CSS

Una regla CSS está formada por un selector y un bloque de declaraciones:

```css
h1 {
    color: #183153;
    font-size: 2rem;
}
```

- `h1` es el **selector**: identifica los elementos a los que se aplica la regla.
- `{ ... }` delimita el bloque de declaraciones.
- `color` y `font-size` son **propiedades**.
- `#183153` y `2rem` son **valores**.
- Cada declaración termina normalmente con punto y coma.

Una propiedad expresa qué aspecto se quiere modificar; el valor concreta cómo.

### Ejemplo explicado

```css
p {
    color: #333333;
    line-height: 1.6;
}
```

El navegador localiza los párrafos, aplica un color gris oscuro al texto y establece una altura de línea de 1,6 veces el tamaño de fuente. La regla no cambia el contenido del párrafo ni su significado.

## 3. Tres formas de incorporar CSS

### 3.1. Hoja externa

En el documento HTML:

```html
<head>
    <meta charset="UTF-8">
    <title>Mi sitio</title>
    <link rel="stylesheet" href="css/estilos.css">
</head>
```

En `css/estilos.css`:

```css
body {
    font-family: Arial, sans-serif;
    color: #222222;
}
```

Es la opción preferente en proyectos reales porque separa archivos, facilita la reutilización y permite mantener un diseño coherente.

La ruta de `href` es relativa al documento HTML. Si el archivo no carga, comprueba primero la ruta, el nombre, las mayúsculas y la ubicación real.

### 3.2. Hoja interna

Se escribe dentro de `style` en `head`:

```html
<head>
    <style>
        h1 {
            color: darkblue;
        }
    </style>
</head>
```

Puede resultar útil en demostraciones pequeñas o documentos aislados. En un sitio con varias páginas tiende a duplicar reglas.

### 3.3. Estilo en línea

Se aplica mediante el atributo `style`:

```html
<p style="color: crimson;">Aviso importante</p>
```

Es rápido para una prueba puntual, pero dificulta la reutilización y mezcla presentación con estructura. No debe convertirse en la estrategia habitual.

## 4. Comparación y decisión

| Método   | Dónde se escribe         | Uso recomendado                |
| -------- | ------------------------ | ------------------------------ |
| Externo  | Archivo `.css` enlazado  | Proyectos y sitios multipágina |
| Interno  | `style` dentro de `head` | Pruebas o documento aislado    |
| En línea | Atributo `style`         | Casos muy puntuales            |

No se trata de que los tres métodos sean equivalentes: cada uno tiene un contexto. En un proyecto mantenible, la hoja externa debe ser la norma.

## 5. Ejemplo guiado: primera página con CSS externo

Estructura:

```text
mi-web/
├── index.html
└── css/
    └── estilos.css
```

`index.html`:

```html
<!doctype html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Club de lectura</title>
    <link rel="stylesheet" href="css/estilos.css">
</head>
<body>
    <h1>Club de lectura</h1>
    <p>Un espacio para compartir libros e ideas.</p>
</body>
</html>
```

`css/estilos.css`:

```css
body {
    font-family: Arial, sans-serif;
    color: #263238;
    background-color: #f5f7fa;
}

h1 {
    color: #174a6e;
}
```

Procedimiento:
1. Crear la carpeta y los dos archivos respetando los nombres.
2. Escribir el HTML sin estilos de presentación.
3. Enlazar la hoja desde `head`.
4. Guardar ambos archivos.
5. Abrir `index.html` en el navegador.
6. Cambiar el color de `h1` en el CSS y comprobar que no hace falta tocar HTML.

Si no cambia nada, verifica que el `link` apunta al archivo correcto y que has guardado el CSS.

## 6. Errores frecuentes

- Escribir `href="estilos.css"` cuando el archivo está dentro de `css/`.
- Olvidar cerrar una llave `}`.
- Escribir `font-size: 20;` sin unidad cuando la propiedad necesita una longitud.
- Guardar el archivo como `estilos.css.txt`.
- Colocar `link` dentro de `body` en lugar de `head`.
- Confundir el nombre del archivo con el nombre de la carpeta.

## 7. Actividades

**E01. Identificación.** En la regla `h2 { color: teal; margin-bottom: 1rem; }`, identifica selector, propiedades y valores.

**E02. Decisión técnica.** Una web tiene doce páginas y todas deben compartir tipografía y colores. Explica qué método de incorporación elegirías y por qué.

**E03. Estructura.** Crea `index.html` y `css/estilos.css`. Enlaza correctamente la hoja externa.

**E04. Experimentación.** Añade reglas para el fondo de `body`, el color de `h1` y el tamaño de los párrafos. Modifica después un valor sin tocar HTML.

**E05. Diagnóstico.** Se proporciona una página cuyo CSS no se aplica. Revisa ruta, ubicación del `link`, nombre del fichero y sintaxis.

## 8. Reto práctico

Construye la portada de una pequeña academia con título, descripción y tres enlaces. Toda la presentación debe estar en una hoja externa. No se permite utilizar `style` en línea.

## 9. Comprobación final

- [ ] Distingo estructura HTML y presentación CSS.
- [ ] Reconozco selector, propiedad y valor.
- [ ] Sé enlazar una hoja externa.
- [ ] Puedo explicar cuándo tendría sentido una hoja interna o un estilo en línea.
- [ ] Sé localizar un error sencillo de carga de CSS.
