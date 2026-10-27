# Guía Completa de Clase: Introducción a Flexbox vs. CSS Grid (UP4)

**Módulo:** Diseño de Interfaces Web (DIW) — 2º DAW  
**Unidad de Programación:** UP4 – CSS3 Avanzado, Grid/Flex y Responsive Web Design  
**Duración de la sesión:** 2 Horas (Horas 1 y 2 de 16)  
**Resultado de Aprendizaje:** RA02 – Crea interfaces web homogéneas definiendo y aplicando estilos  

---

## ⏱️ Estructura y Planificación de la Sesión de 2 Horas

* **00 - 15 min:** Presentación de la UP4 y evolución histórica de la maquetación web.
* **15 - 45 min:** Bloque 1 – Flexbox: Conceptos clave, ejes (Main/Cross) y propiedades.
* **45 - 80 min:** Bloque 2 – CSS Grid: Conceptos clave, unidades (`fr`), `minmax`, `repeat` y `grid-template-areas`.
* **80 - 100 min:** Bloque 3 – Cuadro comparativo y reglas de decisión técnica en proyectos web realistas.
* **100 - 120 min:** Demostración práctica en directo (Live Coding) y resolución de dudas iniciales del alumnado.

---

# PARTE 1: Explicación Teórica para el Aula

## 1. Evolución de la Maquetación Web
* **Mapeo histórico:** Antes de Flexbox/Grid, la maquetación se realizaba mediante `float: left`, tablas HTML o `display: inline-block`. Esos sistemas generaban problemas de colapso de contenedores, falta de alineación vertical limpia y cálculos manuales de márgenes.
* **La maquetación moderna:** W3C introdujo **Flexbox** (orientado a componentes unidimensionales) y **CSS Grid** (orientado a estructuras bidimensionales).

---

## 2. Flexbox: Maquetación Unidimensional (1D)

### Concepto Intuitivo
Pensar en Flexbox como **elementos colocados a lo largo de una línea o fila/columna**. Todo pivota sobre la relación entre un **Contenedor Padre** (`display: flex`) y sus **Hijos Directos** (*flex-items*).

### Los Dos Ejes Fundamentales
1. **Eje Principal (`Main Axis`):** Dirección en la que se disponen los elementos (por defecto horizontal, de izquierda a derecha). Se controla con `justify-content`.
2. **Eje Cruzado (`Cross Axis`):** Eje perpendicular al principal (por defecto vertical, de arriba a abajo). Se controla con `align-items`.

```
[EJE PRINCIPAL: justify-content] ------------------------->
   ┌──────────┐   ┌──────────┐   ┌──────────┐
   │  Item 1  │   │  Item 2  │   │  Item 3  │
   └──────────┘   └──────────┘   └──────────┘
        │
        │ [EJE CRUZADO: align-items]
        ▼
```

---

## 3. CSS Grid: Maquetación Bidimensional (2D)

### Concepto Intuitivo
Pensar en CSS Grid como **una cuadrícula o rejilla (como una hoja de cálculo)** con filas y columnas simultáneas.

### Conceptos Clave de Grid
* **Unidad `fr` (Fracción):** Divide el espacio disponible de forma proporcional (ej. `1fr 2fr` asigna 1/3 del espacio a la primera columna y 2/3 a la segunda).
* **Función `repeat()`:** Simplifica la declaración de cuadrículas (ej. `repeat(3, 1fr)`).
* **Función `minmax(mín, máx)`:** Asegura límites de tamaño responsivos sin romper el diseño.
* **`grid-template-areas`:** Permite "dibujar" la maqueta nombrando las zonas entre comillas.

---

# PARTE 2: Cuadro Comparativo y Reglas de Elección

| Criterio | **Flexbox** | **CSS Grid** |
| :--- | :--- | :--- |
| **Dimensión** | **Unidimensional** (Filas O Columnas) | **Bidimensional** (Filas Y Columnas) |
| **Filosofía** | Basado en el **contenido** (los elementos se adaptan) | Basado en el **contenedor** (la rejilla define la posición) |
| **Uso Principal** | Componentes internos (navbars, listas, botones, tarjetas) | Estructura global (*Layout* general: header, sidebar, main, footer) |
| **Alineación** | Ideal para alineación vertical/horizontal rápida en 1 eje | Ideal para cuadrículas complejas y diseños adaptativos |

### Regla Nemotécnica para los Alumnos:
1. **Usa CSS Grid para el ESQUELETO EXTERIOR** de la página web.
2. **Usa Flexbox para ALINEAR LOS ELEMENTOS INTERNOS** dentro de cada sección.

---

# PARTE 3: Cheat Sheet – Listado Completo de Propiedades y Valores

## A. FLEXBOX

### Propiedades del Padre (`Flex Container`)

* **`display`**:
  * `flex`: Convierte el contenedor en bloque flex.
  * `inline-flex`: Convierte el contenedor en elemento en línea flex.
* **`flex-direction`** (Eje Principal):
  * `row` *(por defecto)*: Fila horizontal (izquierda a derecha).
  * `column`: Columna vertical (arriba a abajo).
  * `row-reverse`: Fila horizontal invertida.
  * `column-reverse`: Columna vertical invertida.
* **`justify-content`** (Alineación Eje Principal):
  * `flex-start` *(por defecto)*: Alinea al inicio.
  * `flex-end`: Alinea al final.
  * `center`: Centra los elementos.
  * `space-between`: Pega extremos y reparte el espacio central.
  * `space-around`: Margen uniforme alrededor de cada elemento.
  * `space-evenly`: Espaciado exactamente igual entre elementos y bordes.
* **`align-items`** (Alineación Eje Cruzado):
  * `stretch` *(por defecto)*: Estira los elementos al alto/ancho total.
  * `center`: Centrado vertical.
  * `flex-start`: Alinea arriba.
  * `flex-end`: Alinea abajo.
  * `baseline`: Alinea según la línea base del texto.
* **`flex-wrap`**:
  * `nowrap` *(por defecto)*: Fuerza a estar en 1 sola línea.
  * `wrap`: Permite salto a siguiente línea.
* **`gap`**: Define la distancia entre ítems (ej. `15px`, `1rem`).

### Propiedades de los Hijos (`Flex Items`)
* **`flex-grow`**: Factor de crecimiento (ej. `0` no crece, `1` crece ocupando espacio sobrante).
* **`flex-shrink`**: Factor de contracción (ej. `1` se encoge si no cabe, `0` mantiene tamaño fijo).
* **`flex-basis`**: Tamaño inicial antes de repartir espacio (ej. `auto`, `200px`).
* **`flex`** *(Shorthand)*: Agrupa `grow shrink basis` (ej. `flex: 1;` = `1 1 0%`).

---

## B. CSS GRID

### Propiedades del Padre (`Grid Container`)

* **`display`**: `grid` | `inline-grid`.
* **`grid-template-columns`**:
  * Unidades: `px`, `%`, `em`, `rem`, `fr`.
  * `repeat(número, tamaño)`: Ej. `repeat(3, 1fr)`.
  * `minmax(mín, máx)`: Ej. `minmax(200px, 1fr)`.
  * `auto-fit` / `auto-fill`: Rejilla adaptable dinámica.
* **`grid-template-rows`**: Define filas (ej. `100px auto 50px`).
* **`grid-template-areas`**: Mapa gráfico de nombres (ej. `"header header" "sidebar main" "footer footer"`).
* **`gap`**: Distancia entre filas y columnas (ej. `20px`).

### Propiedades de los Hijos (`Grid Items`)
* **`grid-area`**: Asigna el nombre de la zona (ej. `grid-area: header;`).
* **`grid-column`**: Extensión de columnas (ej. `1 / 3` o `span 2`).
* **`grid-row`**: Extensión de filas.

---

# PARTE 4: Códigos de Demostración para el Profesor (Live Coding)

## Código 1: Demostración Flexbox (`demo-flex.html`)
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Demostración Flexbox - Profesor</title>
  <style>
    .navbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      background-color: #0f172a;
      padding: 15px 30px;
      color: #ffffff;
      font-family: Arial, sans-serif;
    }

    .menu-links {
      display: flex;
      gap: 20px;
      list-style: none;
      margin: 0;
      padding: 0;
    }

    .menu-links a {
      color: #38bdf8;
      text-decoration: none;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <nav class="navbar">
    <div class="brand"><h2>MiPortalWeb</h2></div>
    <ul class="menu-links">
      <li><a href="#">Inicio</a></li>
      <li><a href="#">Servicios</a></li>
      <li><a href="#">Contacto</a></li>
    </ul>
  </nav>
</body>
</html>
```

## Código 2: Demostración CSS Grid (`demo-grid.html`)
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Demostración CSS Grid - Profesor</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 0; }

    .app-layout {
      display: grid;
      grid-template-columns: 240px 1fr;
      grid-template-rows: 80px 450px 60px;
      grid-template-areas:
        "cabecera cabecera"
        "lateral   contenido"
        "pie       pie";
      gap: 12px;
      padding: 12px;
      background-color: #e2e8f0;
    }

    header { grid-area: cabecera; background-color: #1e293b; color: white; padding: 20px; }
    aside  { grid-area: lateral;  background-color: #0284c7; color: white; padding: 20px; }
    main   { grid-area: contenido; background-color: #ffffff; padding: 20px; }
    footer { grid-area: pie;       background-color: #334155; color: white; padding: 15px; }
  </style>
</head>
<body>
  <div class="app-layout">
    <header><h1>Cabecera Global (Header)</h1></header>
    <aside><h3>Menú Lateral (Sidebar)</h3></aside>
    <main><h2>Área Principal (Main Content)</h2><p>Contenido explicativo de la sesión...</p></main>
    <footer><p>Pie de Página (Footer)</p></footer>
  </div>
</body>
</html>
```
