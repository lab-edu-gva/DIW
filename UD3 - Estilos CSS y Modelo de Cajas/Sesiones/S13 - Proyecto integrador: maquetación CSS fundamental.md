# S13 · Proyecto integrador: maquetación CSS fundamental

---
asignatura: DIW
unidad: UD3
sesion: 13
tipo: material-alumnado
estado: preparado
publicar: true
---

## 1. Objetivo

Construir una página informativa completa aplicando los fundamentos de CSS trabajados en la unidad. El objetivo no es producir una web compleja, sino demostrar que se sabe organizar una hoja de estilos, seleccionar elementos, controlar tipografía y color, calcular cajas y resolver problemas básicos de presentación.

## 2. Escenario

Una asociación cultural necesita una página para anunciar sus actividades. Debe incluir:
- Cabecera con nombre y descripción.
- Navegación sencilla.
- Contenido principal con varias actividades.
- Una tarjeta destacada.
- Información secundaria.
- Pie de página.

El contenido HTML debe tener una estructura comprensible. La presentación se realizará desde una hoja CSS externa.

## 3. Requisitos técnicos

1. Crear `index.html` y `css/estilos.css`.
2. Enlazar correctamente la hoja externa.
3. Utilizar selectores de tipo y clases.
4. Definir una escala tipográfica.
5. Aplicar colores coherentes con valores HEX, RGB o HSL.
6. Utilizar `padding`, `border` y `margin` con una intención clara.
7. Aplicar `box-sizing: border-box`.
8. Controlar `display` cuando sea necesario.
9. Resolver un caso de overflow si aparece.
10. Utilizar posicionamiento solo para un elemento que lo justifique.
11. Comprobar el resultado en el navegador y corregir errores.

Flexbox y Grid pueden utilizarse porque ya se han trabajado en clase, pero el proyecto debe mostrar que el alumnado entiende el modelo de cajas y el flujo básico. No se evaluará como contenido nuevo el dominio avanzado de Grid/Flex, que corresponde a la UD4.

## 4. Estructura inicial sugerida

```text
asociacion/
├── index.html
└── css/
    └── estilos.css
```

HTML inicial:

```html
<!doctype html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Asociación Cultural</title>
    <link rel="stylesheet" href="css/estilos.css">
</head>
<body>
    <header class="cabecera">
        <h1>Asociación Cultural</h1>
        <p>Actividades para aprender y compartir.</p>
    </header>

    <nav class="navegacion" aria-label="Navegación principal">
        <a href="#actividades">Actividades</a>
        <a href="#informacion">Información</a>
    </nav>

    <main>
        <section id="actividades">
            <h2>Próximas actividades</h2>
            <article class="tarjeta destacada">
                <h3>Taller de fotografía</h3>
                <p>Una introducción práctica a la fotografía.</p>
            </article>
            <article class="tarjeta">
                <h3>Club de lectura</h3>
                <p>Un encuentro mensual para compartir lecturas.</p>
            </article>
        </section>

        <aside id="informacion">
            <h2>Más información</h2>
            <p>Consulta las actividades y horarios.</p>
        </aside>
    </main>

    <footer class="pie">
        <p>Asociación Cultural · 2026</p>
    </footer>
</body>
</html>
```

## 5. Secuencia de trabajo recomendada

### Fase 1. Organización
- Crea las carpetas y archivos.
- Comprueba que el HTML abre correctamente.
- Verifica que la hoja externa se carga.

### Fase 2. Estilos generales
- Define `box-sizing`.
- Establece tipografía y color de texto.
- Configura el fondo general.
- Crea una paleta limitada.

### Fase 3. Componentes
- Aplica estilos a cabecera, navegación, tarjetas y pie.
- Reutiliza clases.
- Evita reglas duplicadas.
- Ajusta padding, borde y margen.

### Fase 4. Comportamientos
- Revisa `display`.
- Comprueba el desbordamiento.
- Incorpora posicionamiento solo si aporta una función clara.

### Fase 5. Verificación
- Inspecciona cajas en herramientas de desarrollador.
- Comprueba enlaces.
- Busca desbordamientos.
- Revisa que no haya contenido oculto.
- Comprueba la legibilidad.

## 6. Entregables

- `index.html`
- `css/estilos.css`
- Captura de pantalla del resultado.
- Breve explicación de las decisiones de CSS.
- Lista de dos problemas encontrados y cómo se resolvieron.

## 7. Lista de comprobación

- [ ] La hoja externa está enlazada.
- [ ] El HTML conserva estructura y contenido.
- [ ] Las clases son reutilizables y tienen nombres claros.
- [ ] La tipografía establece jerarquías.
- [ ] Los colores son coherentes y legibles.
- [ ] El modelo de cajas está controlado.
- [ ] No hay desbordamientos inesperados.
- [ ] El posicionamiento tiene una finalidad concreta.
- [ ] El resultado se ha probado en el navegador.

## 8. Reflexión final

Responde:
1. ¿Qué diferencia práctica existe entre padding y margin?
2. ¿Por qué `border-box` facilita calcular anchuras?
3. ¿Qué diferencia existe entre `display:none` y `overflow:hidden`?
4. ¿Cuándo elegirías `relative` y cuándo `absolute`?
5. ¿Qué problema resolverías mediante una hoja externa en lugar de estilos en línea?
