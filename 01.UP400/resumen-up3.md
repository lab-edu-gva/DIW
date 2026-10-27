# Resumen de la Unidad de Programación 3 (UP3): Estilos CSS y Modelo de Cajas

**Módulo:** Diseño de Interfaces Web (DIW) — 2º CFGS Desarrollo de Aplicaciones Web (DAW)  
**Centro:** IES Miguel Ballesteros Viana (Utiel) | **Curso:** 2026-2027  
**Duración:** 12 horas lectivas (1er Trimestre)  
**Resultado de Aprendizaje:** RA02 – Crea interfaces web homogéneas definiendo y aplicando estilos  

---

## 1. Fundamentos y Sintaxis Básica de CSS

* **Principio de Separación de Responsabilidades:** HTML5 se encarga de la estructura y semántica del documento, mientras que CSS3 controla la presentación y capa visual.
* **Sintaxis de las Reglas de Estilo:**
  ```css
  selector {
    propiedad: valor;
  }
  ```
* **Métodos de Asociación de CSS al Documento HTML:**
  1. **Hoja Externa (Recomendada):** Enlace mediante la etiqueta `<link rel="stylesheet" href="estilos.css">` en el `<head>`.
  2. **Estilos Embebidos:** Dentro de un bloque `<style>` en la cabecera HTML.
  3. **Estilos en Línea (Evitar):** Mediante el atributo `style="..."` directamente en las etiquetas HTML.
* **Selectores Básicos:**
  * *Selector de Etiqueta / Tipo:* Aplica a todos los elementos del mismo tipo (ej. `p`, `h1`).
  * *Selector de Clase (`.nombre`):* Reutilizable en múltiples elementos (`class="nombre"`).
  * *Selector de ID (`#nombre`):* Único por documento HTML (`id="nombre"`).
* **Propiedades de Texto y Color:**
  * *Tipografía:* `font-family`, `font-size`, `font-weight`, `line-height`, `text-align`.
  * *Modelos de Color:* Nombres de color, Hexadecimal (`#HEX`), RGB/RGBA (`rgba(r, g, b, a)`), HSL.

---

## 2. El Modelo de Cajas (*Box Model*)

En CSS, todos los elementos HTML son representados como **cajas rectangulares** compuestas por cuatro capas concéntricas (de dentro hacia afuera):

1. **`content` (Contenido):** Área donde se muestra el texto, imagen u otros elementos hijos.
2. **`padding` (Relleno):** Espacio interno transparente entre el contenido y el borde.
3. **`border` (Borde):** Línea decorativa que delimita el relleno y el contenido.
4. **`margin` (Margen):** Espacio externo transparente que separa la caja de otros elementos colindantes.

### La propiedad `box-sizing`
* **`box-sizing: content-box;` (Por defecto):** El ancho y alto especificados aplican solo al contenido. El ancho total visible se calcula como: `width + padding + border`.
* **`box-sizing: border-box;` (Estándar Profesional):** El ancho y alto definidos engloban el contenido, el padding y el borde, evitando desbordamientos no deseados.

---

## 3. Visualización y Esquemas de Posicionamiento

### Tipos de Visualización (`display`)
* **`block`:** Ocupa todo el ancho disponible y fuerza un salto de línea (ej. `<div>`, `<article>`, `<p>`).
* **`inline`:** Ocupa solo el espacio de su contenido e ignora dimensiones fijas y márgenes verticales (ej. `<span>`, `<a>`).
* **`inline-block`:** Se alinea en flujo horizontal pero permite configurar `width`, `height`, `padding` y `margin`.
* **`none`:** Oculta el elemento y lo elimina del flujo visual del documento.

### Posicionamiento (`position`)
* **`static`:** Posicionamiento por defecto según el flujo normal del HTML.
* **`relative`:** Permite desplazar la caja mediante `top`, `bottom`, `left`, `right` respecto a su posición original sin alterar el flujo de los demás elementos.
* **`absolute`:** Extrae el elemento del flujo y lo posiciona respecto a su ancestro posicionado más cercano (`position` distinto de `static`).
* **`fixed`:** Posiciona la caja de forma fija respecto a la ventana del navegador (`viewport`).
* **`sticky`:** Alterna entre `relative` y `fixed` según el desplazamiento de la página (*scroll*).

### Capas y Control de Desbordamiento
* **`z-index`:** Controla la superposición de elementos posicionados en el eje Z.
* **`overflow`:** Gestiona el contenido que excede las dimensiones de la caja (`visible`, `hidden`, `scroll`, `auto`).

---

## 4. Prácticas y Retos Desarrollados en el Aula

1. **Práctica 1: Vinculación Externa y Estilos Globales:** Creación de hojas de estilo externas, selectores de clase y formato tipográfico.
2. **Práctica 2: Experimentación del Modelo de Cajas:** Inspección mediante F12 para comparar el comportamiento de `content-box` y `border-box`.
3. **Práctica 3: Componente de Tarjeta de Perfil/Producto:** Maquetación completa de un bloque informativo utilizando bordes, rellenos, sombras y botones estilizados.
4. **Práctica 4 (Evaluativa - Reto "Bug Hunter"):** Tarea autónoma de depuración de código con el inspector F12 para resolver errores reales de desbordamiento, context de posicionamiento absoluto y comportamiento de enlaces mediante `display: inline-block`.

---

## 5. Evaluación y Validación

* **Validación de Código:** Comprobación de cumplimiento de estándares CSS mediante el **Validador W3C**.
* **Resultado de Aprendizaje 2 (RA02):** Vinculación directa con los criterios de evaluación de hojas externas, modificación de propiedades, creación de clases, redefinición de estilos y aplicación de guías de estilo.
