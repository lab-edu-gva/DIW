# Tabla de Ejercicios Prácticos: Flexbox y CSS Grid (UP4)

**Módulo:** Diseño de Interfaces Web (DIW)  
**Unidad de Programación:** UP4 – CSS3 Avanzado, Flexbox, Grid Layout y Responsive Web Design  
**Resultado de Aprendizaje:** RA02 – Crea interfaces web homogéneas definiendo y aplicando estilos  
**Plataforma de entrega:** Aules  

---

## 📊 Resumen General de Ejercicios (De menor a mayor dificultad)

| Nivel | Nombre del Ejercicio | Tecnología | Conceptos Clave | Tiempo Estimado |
| :--- | :--- | :--- | :--- | :--- |
| **1. Muy Fácil** | Barra de Navegación Simple | Flexbox | `display: flex`, `justify-content: space-between`, `align-items: center`, `gap` | 15 - 20 min |
| **2. Fácil** | Tarjeta de Perfil Vertical | Flexbox | `flex-direction: column`, `align-items: center`, `gap` | 20 - 25 min |
| **3. Intermedio-Bajo** | Galería de Imágenes Simétrica | CSS Grid | `display: grid`, `grid-template-columns`, unidad `fr`, `gap` | 25 - 30 min |
| **4. Intermedio** | Tabla Comparativa de Precios | Flexbox | `flex-grow`, `flex-basis`, `align-items: stretch` | 35 - 45 min |
| **5. Intermedio-Alto** | Esqueleto de Sitio Web (Layout) | CSS Grid | `grid-template-areas`, `grid-template-rows`, `grid-template-columns` | 45 - 60 min |
| **6. Difícil** | Dashboard de Administración | Grid + Flexbox | Combinación de **Grid** (layout global) y **Flexbox** (componentes internos) | 60 - 75 min |
| **7. Muy Difícil** | Tienda Responsive sin Media Queries | CSS Grid + Flex | `repeat()`, `auto-fit`, `minmax()`, componentes flex anidados | 75 - 90 min |

---

## 📝 Detalle de Enunciados por Nivel

### Nivel 1: Barra de Navegación Simple (Flexbox)
* **Objetivo:** Empujar el logo a la izquierda y la lista de enlaces a la derecha.
* **Requisitos:**
  - Contenedor `<header>` con clase `.navbar`.
  - Aplicar `display: flex`, `justify-content: space-between` y `align-items: center`.
  - Usar `gap: 20px` para separar los elementos de la lista `<ul>`.

### Nivel 2: Tarjeta de Perfil Vertical (Flexbox)
* **Objetivo:** Apilar elementos verticalmente y alinearlos al centro.
* **Requisitos:**
  - Contenedor `<article>` con clase `.card`.
  - Usar `flex-direction: column` y `align-items: center`.
  - Incluir imagen circular (`border-radius: 50%`), título `<h2>`, descripción `<p>` y botón `<a>`.

### Nivel 3: Galería de Imágenes Simétrica (CSS Grid)
* **Objetivo:** Crear una rejilla de 3x3 imágenes de igual tamaño.
* **Requisitos:**
  - Contenedor `<section>` con clase `.galeria`.
  - Definir `grid-template-columns: repeat(3, 1fr)`.
  - Aplicar `gap: 15px` entre celdas.

### Nivel 4: Tabla Comparativa de Precios (Flexbox)
* **Objetivo:** Destacar una tarjeta de precio haciéndola más grande que las demás.
* **Requisitos:**
  - 3 tarjetas dentro de un contenedor `display: flex`.
  - La tarjeta central ("Plan Pro") debe llevar `flex-grow: 1.2` o mayor padding/transformación visual.
  - Asegurar alineación uniforme con `align-items: stretch`.

### Nivel 5: Esqueleto de Sitio Web (CSS Grid Areas)
* **Objetivo:** Maquetar la estructura global de una página web dibujando áreas.
* **Requisitos:**
  - Usar `grid-template-areas` con los nombres `"header header"`, `"sidebar main"`, `"footer footer"`.
  - Asignar `grid-area` a `<header>`, `<aside>`, `<main>` y `<footer>`.

### Nivel 6: Dashboard de Administración (Grid + Flexbox)
* **Objetivo:** Combinar las dos tecnologías en un proyecto completo.
* **Requisitos:**
  - **CSS Grid** para la rejilla de paneles del panel de control.
  - **Flexbox** dentro de cada tarjeta para alinear iconos, estadísticas y botones de acción.

### Nivel 7: Tienda Responsive sin Media Queries (Grid Avanzado)
* **Objetivo:** Lograr adaptabilidad automática total a cualquier resolución de pantalla.
* **Requisitos:**
  - Rejilla con `grid-template-columns: repeat(auto-fit, minmax(250px, 1fr))`.
  - Tarjetas de producto maquetadas internamente con Flexbox.
