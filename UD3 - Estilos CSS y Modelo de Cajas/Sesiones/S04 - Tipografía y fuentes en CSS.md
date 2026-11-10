# S04 · Tipografía y fuentes en CSS

---
asignatura: DIW
unidad: UD3
sesion: 4
tipo: material-alumnado
estado: preparado
publicar: true
---

## 1. La tipografía también es interfaz

La tipografía condiciona la legibilidad, la jerarquía de la información y la personalidad visual de una interfaz. No basta con elegir una fuente atractiva: debe funcionar en el dispositivo, en distintos tamaños y con el contenido real.

En una interfaz, la tipografía debe ayudar a responder rápidamente:
- ¿Cuál es el título principal?
- ¿Qué información es secundaria?
- ¿Dónde comienza un bloque?
- ¿Qué texto requiere atención?

## 2. `font-family`

Define la familia tipográfica:

```css
body {
    font-family: Arial, Helvetica, sans-serif;
}
```

La lista se interpreta de izquierda a derecha. Si la primera fuente no está disponible, el navegador prueba la siguiente. Conviene terminar con una familia genérica como `serif`, `sans-serif` o `monospace`.

Los nombres de familias con espacios se escriben entre comillas:

```css
h1 {
    font-family: "Trebuchet MS", sans-serif;
}
```

## 3. `font-size`

Controla el tamaño del texto. Puede expresarse en distintas unidades.

```css
h1 {
    font-size: 2rem;
}

p {
    font-size: 1rem;
}
```

- `px`: unidad absoluta en CSS, aunque su representación física depende del dispositivo y del navegador.
- `em`: relativo al tamaño de fuente del contexto.
- `rem`: relativo al tamaño de fuente del elemento raíz (`html`).

`rem` facilita definir una escala tipográfica coherente. No existe una unidad universalmente correcta: importa entender la referencia de cada una.

## 4. `font-weight`

Define el grosor:

```css
h1 {
    font-weight: 700;
}

p {
    font-weight: 400;
}
```

Valores habituales:
- `400`: normal.
- `700`: negrita.
- `100` a `900`: pesos numéricos, si la fuente dispone de ellos.
- `bold` y `normal`: palabras clave.

Solicitar un peso que la fuente no ofrece puede producir una aproximación del navegador.

## 5. `font-style`

Permite usar estilos como normal o cursiva:

```css
em {
    font-style: italic;
}
```

No debe confundirse el significado semántico de `em` en HTML con la decisión visual de cursiva. HTML aporta significado; CSS controla la presentación.

## 6. Fuentes del sistema y fuentes web

Las fuentes del sistema evitan descargas adicionales y suelen ser una opción robusta. Las fuentes web permiten una identidad visual más específica, pero añaden consideraciones de rendimiento, licencias y disponibilidad.

En esta unidad se priorizará el uso de fuentes instaladas y pilas de fuentes seguras. La integración avanzada de fuentes externas puede abordarse como ampliación.

## 7. Ejemplo guiado: escala tipográfica

```css
html {
    font-size: 16px;
}

body {
    font-family: Arial, Helvetica, sans-serif;
    font-size: 1rem;
}

h1 {
    font-size: 2rem;
    font-weight: 700;
}

h2 {
    font-size: 1.5rem;
    font-weight: 700;
}

p {
    font-size: 1rem;
    font-weight: 400;
}
```

Con una raíz de 16 píxeles, `1rem` equivale a 16 píxeles y `2rem` a 32 píxeles. Si se modifica el tamaño de fuente raíz, las medidas expresadas en `rem` se ajustan proporcionalmente.

## 8. Buenas prácticas

- Utilizar pocas familias tipográficas.
- Crear una escala de tamaños consistente.
- Reservar pesos intensos para jerarquías reales.
- Comprobar la lectura en pantallas pequeñas.
- Mantener contraste suficiente entre texto y fondo.
- No utilizar el tamaño como único indicador de importancia.

## 9. Errores frecuentes

- Escribir `font-family: Arial` sin alternativa.
- Utilizar demasiadas fuentes distintas.
- Aplicar tamaños diminutos a textos secundarios.
- Confundir `font-weight` con `font-size`.
- Suponer que `2em` siempre equivale a 32 píxeles.

## 10. Actividades

**E15. Interpretación.** Explica qué hace cada declaración de una regla que contiene `font-family`, `font-size` y `font-weight`.

**E16. Conversión.** Si el tamaño raíz es 16 px, calcula el tamaño equivalente de `1.25rem`, `1.5rem` y `2rem`.

**E17. Diseño.** Define una escala tipográfica para título, subtítulo, texto normal y nota secundaria.

**E18. Revisión.** Analiza una página con cinco familias tipográficas y propone una simplificación justificada.

## 11. Reto práctico

Aplica una jerarquía tipográfica completa a una página de noticias. Debe distinguirse claramente el titular, la entradilla, el cuerpo y la información auxiliar.

## 12. Comprobación final

- [ ] Selecciono una pila de fuentes con alternativas.
- [ ] Distingo `px`, `em` y `rem`.
- [ ] Configuro tamaño, peso y estilo.
- [ ] Justifico una escala tipográfica coherente.
