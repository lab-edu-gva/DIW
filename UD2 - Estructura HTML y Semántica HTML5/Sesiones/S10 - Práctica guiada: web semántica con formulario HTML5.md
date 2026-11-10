---
asignatura: DIW
unidad: UD2
sesion: 10
tipo: material-alumnado
estado: preparado
programacion: "UP2 - Estructura HTML y Semántica HTML5"
duracion: "55 minutos"
---

# Sesión 10 · Práctica guiada: web semántica con formulario HTML5

> [!abstract] Propósito de la sesión
> Integrar estructura HTML5, semántica y formularios en un documento coherente.

## Objetivos de aprendizaje
- Planificar la estructura antes de escribir el código.
- Combinar regiones semánticas y contenido textual.
- Integrar un formulario HTML5 con controles y validación.

## Desarrollo de contenidos

## 1. Enunciado del proyecto

Vas a crear la página de una jornada de puertas abiertas de un centro educativo. La página debe informar sobre el evento y permitir que una persona solicite una plaza.

## 2. Requisitos estructurales

El documento debe incluir:

- Estructura HTML5 completa.
- Idioma principal español y metadatos básicos.
- `header` con el nombre del centro y el título de la actividad.
- `nav` con enlaces internos a las secciones de la página.
- Un único `main` con la información principal.
- Al menos una `section` temática.
- Al menos un `article` que contenga información autónoma del evento.
- Un `aside` con información complementaria.
- `footer` con datos de contacto o autoría.

## 3. Requisitos del formulario

El formulario debe recoger:

- Nombre y apellidos.
- Correo electrónico.
- Fecha preferida para asistir.
- Ciclo formativo de interés mediante `select`.
- Número de acompañantes mediante `number`.
- Nivel de interés mediante `range`.
- Observaciones mediante `textarea`.

Incluye `label` asociados, atributos `id` y `name`, y validaciones razonables. No se exige programar un servidor.

## 4. Planificación previa

Antes de programar, realiza un esquema de las regiones y decide qué contenido corresponde a cada elemento. No empieces escribiendo etiquetas al azar: una estructura pensada evita tener que reconstruir el documento.

## 5. Comprobaciones

- Abre el archivo en el navegador.
- Comprueba que los enlaces internos llevan a la sección correcta.
- Prueba los controles del formulario.
- Comprueba los campos obligatorios y los límites numéricos.
- Valida el documento con el validador W3C.
- Corrige los errores y vuelve a validar.

## 6. Alcance

No se evaluará el diseño visual mediante CSS en esta práctica. El objetivo es la estructura, el significado de los elementos y el funcionamiento nativo de los controles HTML.

## Ejemplo guiado

### Secuencia de trabajo recomendada

1. Crear carpeta y archivo `index.html`.
2. Escribir la estructura mínima.
3. Añadir las regiones semánticas.
4. Incorporar los contenidos y encabezados.
5. Crear el formulario y asociar las etiquetas.
6. Añadir restricciones de validación.
7. Probar en navegador y validar el código.

## Actividades prácticas

### E37 · Esquema de la página

Dibuja un mapa de regiones y contenidos. Indica qué elemento HTML utilizarás en cada zona y justifica tres decisiones.

### E38 · Construcción incremental

Implementa primero la estructura global y después las secciones, artículos y contenido complementario. Guarda una versión al terminar cada fase.

### E39 · Formulario completo

Implementa todos los controles requeridos. Comprueba que cada `label` apunta al `id` correcto y que los campos que se enviarán tienen `name`.

### E40 · Validación y revisión

Valida el documento, corrige los errores y realiza una revisión cruzada con la lista de comprobación.

## Reto de aplicación

Entrega la página completa con código indentado, nombres de archivo claros y una breve memoria que explique la estructura semántica y las validaciones elegidas.

## Errores que debes evitar

- Elegir etiquetas por su apariencia en lugar de por su significado.
- Escribir código sin revisar el anidamiento.
- Olvidar las etiquetas asociadas a los controles de formulario.
- Dar por válido un documento solo porque el navegador lo muestra.

## Resumen de la sesión

Al finalizar debes poder explicar los conceptos principales, construir un ejemplo pequeño y justificar las decisiones de marcado realizadas.

## Autoevaluación

- [ ] He planificado la estructura antes de programar.
- [ ] He utilizado correctamente las regiones semánticas.
- [ ] El formulario tiene etiquetas asociadas y validaciones.
- [ ] He probado el documento y lo he validado.

## Registro personal

- Dudas que me quedan:
- Errores que he corregido:
- Qué necesito practicar de nuevo:
