# Sesión Práctica: Flexbox vs. CSS Grid (UP4 - 2 Horas)

**Módulo:** Diseño de Interfaces Web (DIW) — 2º DAW  
**Unidad de Programación:** UP4 – CSS3 Avanzado, Grid/Flex y Responsive Web Design  
**Resultado de Aprendizaje:** RA2 – Crea interfaces web homogéneas definiendo y aplicando estilos  

---

## 1. Ejercicio en Vivo para el Profesor: Demo Guiada en Pantalla (30 min)

### 🎯 Objetivo de la Demostración
Mostrar en directo la diferencia práctica entre maquetar una barra de navegación unidimensional (**Flexbox**) y la estructura principal de un panel (**CSS Grid**).

---

### Código HTML de Partida (`index.html`)

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Demo En Vivo: Flexbox vs Grid</title>
  <link rel="stylesheet" href="estilos.css">
</head>
<body>

  <!-- 1. COMPONENTE FLEXBOX: Header con Navegación -->
  <header class="navbar">
    <div class="logo">WebCraft</div>
    <nav class="nav-links">
      <a href="#">Inicio</a>
      <a href="#">Cursos</a>
      <a href="#">Recursos</a>
    </nav>
    <button class="btn-login">Acceder</button>
  </header>

  <!-- 2. COMPONENTE CSS GRID: Layout Principal -->
  <main class="dashboard-grid">
    <aside class="sidebar">
      <h3>Menú Lateral</h3>
      <ul>
        <li>Dashboard</li>
        <li>Proyectos</li>
        <li>Ajustes</li>
      </ul>
    </aside>

    <section class="main-content">
      <h2>Panel Principal</h2>
      <p>Este bloque ocupa el espacio dinámico central.</p>
    </section>

    <div class="card-1">Tarjeta A</div>
    <div class="card-2">Tarjeta B</div>
  </main>

</body>
</html>
```

---

### Pasos de Codificación CSS en Directo (`estilos.css`)

#### Paso 1: Reset Básico
```css
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background-color: #f4f6f9;
  color: #333;
}
```

#### Paso 2: Explicar Flexbox en la Navbar (Eje Horizontal)
*Destacar ante los alumnos:* `display: flex` distribuye los 3 bloques principales (`logo`, `nav-links`, `btn-login`) a lo largo del eje principal.

```css
.navbar {
  display: flex;
  justify-content: space-between; /* Separa logo, links y botón */
  align-items: center;            /* Centrado vertical perfecto */
  background-color: #1e293b;
  color: white;
  padding: 15px 30px;
}

.nav-links {
  display: flex;
  gap: 20px;                      /* Espaciado uniforme sin márgenes sucios */
}

.nav-links a {
  color: #cbd5e1;
  text-decoration: none;
}

.btn-login {
  background-color: #3b82f6;
  color: white;
  border: none;
  padding: 8px 16px;
  border-radius: 6px;
  cursor: pointer;
}
```

#### Paso 3: Explicar CSS Grid en el Layout del Dashboard (2D)
*Destacar ante los alumnos:* `display: grid` con `grid-template-areas` permite definir la estructura global sin tocar el HTML.

```css
.dashboard-grid {
  display: grid;
  grid-template-columns: 240px 1fr 1fr;
  grid-template-rows: auto 200px;
  grid-template-areas:
    "sidebar main main"
    "sidebar card1 card2";
  gap: 20px;
  padding: 30px;
  max-width: 1200px;
  margin: 0 auto;
}

.sidebar {
  grid-area: sidebar;
  background-color: #ffffff;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.05);
}

.main-content {
  grid-area: main;
  background-color: #ffffff;
  padding: 25px;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.05);
}

.card-1 {
  grid-area: card1;
  background-color: #e0f2fe;
  padding: 20px;
  border-radius: 8px;
}

.card-2 {
  grid-area: card2;
  background-color: #fef3c7;
  padding: 20px;
  border-radius: 8px;
}
```

---

## 2. Ejercicios Prácticos para el Alumnado (60 min)

---

### 📝 Ejercicio 1: Barra de Filtros y Tarjetas Flexibles (Flexbox)
**Tiempo:** 25 minutos  
**Modo:** Individual  

**Instrucciones:**  
Maqueta una sección de catálogo donde:
1. Exista una barra superior de filtros (`.filtros`) ordenada con **Flexbox**:
   * Debe contener un campo de búsqueda, tres botones de categoría y un selector desplegable de ordenación.
   * Todos los elementos deben quedar alineados verticalmente al centro.
   * La barra debe permitir que los elementos salten de línea (`flex-wrap: wrap`) si la pantalla se estrecha.
2. Debajo, crea un contenedor de 4 tarjetas de producto (`.tarjeta`).
   * Las tarjetas deben repartirse equitativamente el espacio utilizando la propiedad `flex: 1 1 200px`.

---

### 📝 Ejercicio 2: Galería Fotográfica Adaptativa sin Media Queries (CSS Grid)
**Tiempo:** 25 minutos  
**Modo:** Individual  

**Instrucciones:**  
Maqueta una galería de 6 imágenes/bloques utilizando **CSS Grid**:
1. Define una cuadrícula cuya cantidad de columnas sea **automática y responsiva** utilizando la función `repeat()`, el valor `auto-fit` y la función `minmax(220px, 1fr)`.
2. Asigna un hueco (`gap`) de `16px` entre las imágenes.
3. Haz que la **primera imagen** ocupe 2 columnas y 2 filas utilizando las propiedades `grid-column: span 2` y `grid-row: span 2`.

---

### 🚀 Ejercicio 3 (Reto Avanzado): Toma de Decisión Técnica ("Búsquense la Vida")
**Tiempo:** 10 minutos de diseño/esquema + Trabajo para casa si no finalizan  

**Enunciado:**  
Se pide maquetar el panel de control de un reproductor de música web (estilo Spotify/Apple Music):
* **Requisito 1:** Una barra inferior fija de reproducción con la portada del álbum a la izquierda, controles centrales (Play, Pause, Progress bar) y control de volumen a la derecha.
* **Requisito 2:** El cuerpo principal dividido en tres columnas (Menú de biblioteca, Lista de reproducción central y Detalle del artista a la derecha).

**Pregunta previa obligatoria antes de escribir código:**  
El alumno debe escribir un breve comentario al inicio de su archivo CSS justificando:
* ¿Por qué usará **Flexbox** en el reproductor inferior?
* ¿Por qué usará **CSS Grid** en la división del cuerpo principal?
