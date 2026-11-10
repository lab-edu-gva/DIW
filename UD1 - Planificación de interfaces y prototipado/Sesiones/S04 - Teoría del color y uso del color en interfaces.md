---
asignatura: DIW
unidad: UD1
sesion: 4
tipo: material-alumnado
estado: preparado
---

# S04. Teoría del color y uso del color en interfaces

## 1. Introducción

El color permite identificar elementos, crear relaciones visuales, reforzar una identidad y comunicar estados. Sin embargo, utilizar muchos colores o elegirlos sin un criterio puede producir interfaces confusas.

En esta sesión estudiaremos conceptos básicos de color y los modelos más habituales para describirlo en entornos digitales y gráficos. Aprenderemos a construir una paleta y a asignar funciones a sus colores.

## 2. Objetivos

- Reconocer conceptos básicos de teoría del color.
- Diferenciar tono, saturación y luminosidad.
- Identificar los modelos HEX, RGB, HSL y CMYK.
- Construir una paleta coherente.
- Asignar funciones a los colores de una interfaz.
- Detectar combinaciones que pueden dificultar la lectura.

## 3. Conceptos previos

Conviene conocer contraste, jerarquía visual y consistencia.

## 4. Conceptos básicos del color

### 4.1. Tono

Es lo que normalmente identificamos como el nombre del color: rojo, verde, azul, amarillo, etc.

### 4.2. Saturación

Describe la intensidad o pureza de un color. Un color muy saturado suele resultar más intenso; uno poco saturado se aproxima a un aspecto apagado o grisáceo.

### 4.3. Luminosidad

Indica cuán claro u oscuro es un color.

Estos tres conceptos permiten describir colores con mayor precisión que utilizando únicamente nombres como «azul claro».

## 5. Modelos de representación

### 5.1. RGB

RGB representa el color mediante la combinación de luz roja, verde y azul. Es un modelo aditivo, utilizado en pantallas.

Cada canal suele representarse con valores entre 0 y 255:

- `rgb(255, 0, 0)` representa rojo.
- `rgb(0, 255, 0)` representa verde.
- `rgb(0, 0, 255)` representa azul.
- `rgb(0, 0, 0)` representa negro.
- `rgb(255, 255, 255)` representa blanco.

### 5.2. HEX

HEX expresa los canales RGB mediante notación hexadecimal. Se escribe habitualmente con `#` seguido de seis dígitos o letras.

Ejemplos:

- `#FF0000`: rojo.
- `#00FF00`: verde.
- `#0000FF`: azul.
- `#000000`: negro.
- `#FFFFFF`: blanco.

Cada pareja representa un canal: rojo, verde y azul.

### 5.3. HSL

HSL representa el color mediante:

- Hue (tono).
- Saturation (saturación).
- Lightness (luminosidad).

Ejemplo: `hsl(210, 60%, 45%)`.

Este modelo puede resultar cómodo para crear variantes de un mismo tono modificando saturación o luminosidad.

### 5.4. CMYK

CMYK utiliza cian, magenta, amarillo y negro. Se emplea principalmente en impresión. No debe confundirse con RGB, que describe la mezcla de luz de las pantallas.

Una guía de estilo puede incluir valores HEX o RGB para la web y valores CMYK cuando también se preparan materiales impresos.

## 6. Relaciones entre colores

Una paleta es un conjunto limitado de colores seleccionados para utilizarse de forma coordinada.

Algunas relaciones habituales:

- **Monocromática:** variaciones de un mismo tono.
- **Análoga:** tonos próximos en el círculo cromático.
- **Complementaria:** tonos situados en posiciones opuestas.
- **Triádica:** tres tonos distribuidos de forma equilibrada alrededor del círculo cromático.

Estas relaciones son puntos de partida, no garantías automáticas de buen diseño. Hay que comprobar el resultado y la función de cada color.

## 7. Funciones del color en una interfaz

En lugar de asignar colores al azar, define roles:

| Rol | Uso posible |
|---|---|
| Principal | Identidad y acciones prioritarias |
| Secundario | Acciones o elementos de apoyo |
| Fondo | Superficies principales |
| Superficie | Tarjetas, paneles o formularios |
| Texto | Información principal |
| Texto secundario | Metadatos y aclaraciones |
| Éxito | Confirmaciones |
| Advertencia | Situaciones que requieren atención |
| Error | Problemas o validaciones fallidas |

No es obligatorio utilizar un color diferente para cada rol. La paleta debe ser limitada y coherente.

## 8. Contraste y comunicación

El texto debe distinguirse claramente del fondo. Una combinación puede parecer atractiva y aun así dificultar la lectura.

No comuniques estados únicamente mediante color. Por ejemplo, un error de formulario debe incluir también un mensaje textual o una señal adicional. Así se evita que el significado dependa exclusivamente de la percepción del color.

## 9. Ejemplo guiado: paleta para una plataforma educativa

Una propuesta inicial podría incluir:

- Azul principal para acciones prioritarias.
- Azul claro para elementos de apoyo.
- Fondo casi blanco para el área de lectura.
- Gris oscuro para el texto principal.
- Verde para confirmaciones.
- Rojo para errores.

El siguiente paso consiste en probar la paleta sobre botones, enlaces, tarjetas, formularios y mensajes. Una paleta no está terminada hasta que se comprueba aplicada a componentes reales.

## 10. Actividades

### Nivel 1. Fundamentos

**E10. Modelos de color**

Explica RGB, HEX, HSL y CMYK. Indica cuál utilizarías para una interfaz web y cuál se relaciona principalmente con impresión.

**Objetivo:** distinguir modelos de representación.

**Resultado esperado:** tabla comparativa con definición y ejemplo.

### Nivel 2. Aplicación

**E11. Diseña una paleta**

Crea una paleta para una web de una biblioteca. Define al menos seis roles de color e indica el valor HEX de cada uno.

Aplica la paleta a un ejemplo de cabecera, botón, tarjeta y mensaje de aviso.

**Objetivo:** crear una paleta funcional y coherente.

**Resultado esperado:** tabla de roles y una muestra de aplicación.

### Nivel 3. Razonamiento

**E12. Diagnóstico de color**

Una web utiliza texto amarillo sobre fondo blanco, botones rojos, verdes y morados sin distinguir su función y mensajes de error indicados solo con color.

Explica los problemas y plantea una solución.

**Objetivo:** valorar el color como recurso de comunicación.

**Resultado esperado:** diagnóstico con mejoras justificadas.

## 11. Reto: sistema de color

Diseña una paleta para una aplicación de reservas de instalaciones deportivas. Debe distinguir acciones principales, información secundaria, fondos y estados.

Entrega los valores HEX y explica el papel de cada color. Comprueba que los textos se distinguen de sus fondos.

## 12. Errores frecuentes

- Utilizar demasiados colores principales.
- Confundir RGB con CMYK.
- Elegir colores solo por gusto personal.
- Utilizar el color como único indicador de estado.
- No comprobar el contraste en componentes reales.
- Definir una paleta sin especificar para qué sirve cada color.

## 13. Buenas prácticas

- Define roles antes de elegir valores.
- Limita la paleta.
- Mantén consistencia entre pantallas.
- Comprueba texto, botones, enlaces y avisos.
- No dependas exclusivamente del color para transmitir información.
- Documenta los valores exactos en la guía de estilo.

## 14. Resumen

El color tiene propiedades como tono, saturación y luminosidad. RGB, HEX y HSL se utilizan para describir colores en entornos digitales; CMYK se relaciona principalmente con impresión. Una paleta funcional asigna roles claros y debe comprobarse en componentes reales.

## 15. Autoevaluación

1. ¿Qué representa cada canal de RGB?
2. ¿Qué significa cada pareja de dígitos en HEX?
3. ¿Qué componentes forman HSL?
4. ¿Para qué se utiliza CMYK?
5. ¿Por qué una paleta necesita roles?
6. ¿Por qué no debe comunicarse un error solo mediante color?

## 16. Checklist

- [ ] Diferencio tono, saturación y luminosidad.
- [ ] Puedo interpretar un color HEX.
- [ ] Distingo RGB, HSL y CMYK.
- [ ] Creo una paleta con roles.
- [ ] Compruebo el contraste y la claridad de los estados.
