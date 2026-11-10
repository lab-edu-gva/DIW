---
asignatura: DIW
unidad: UD1
sesion: 6
tipo: material-alumnado
estado: preparado
---

# S06. Componentes visuales y patrones de interfaz

## 1. Introducción

Las interfaces suelen repetir elementos: botones, campos, tarjetas, menús, avisos o paneles. Diseñar cada uno desde cero en cada pantalla provoca incoherencias y dificulta el mantenimiento.

Un componente visual es una unidad de interfaz que cumple una función reconocible. En esta sesión aprenderemos a identificar componentes, describir su propósito y definir reglas para que puedan reutilizarse.

## 2. Objetivos

- Reconocer componentes habituales de una interfaz.
- Diferenciar contenido, componente y patrón de composición.
- Describir la función y las partes de un componente.
- Definir variantes y estados básicos.
- Aplicar consistencia a un conjunto de pantallas.

## 3. Conceptos previos

Debes conocer los principios de consistencia, proximidad, jerarquía visual y las guías de estilo.

## 4. ¿Qué es un componente?

Es una unidad visual y funcional que puede identificarse y reutilizarse. Por ejemplo, un botón permite ejecutar una acción; una tarjeta agrupa información; un campo permite introducir datos.

Un componente no se define únicamente por su aspecto. También hay que conocer su función, contenido, comportamiento esperado y contexto de uso.

## 5. Componentes frecuentes

### 5.1. Botones

Representan acciones. Deben utilizar etiquetas claras y diferenciar su importancia.

Variantes habituales:

- Principal: acción prioritaria.
- Secundario: acción alternativa.
- Terciario o discreto: acción de menor énfasis.
- Destructivo: acción que puede eliminar o modificar datos de forma importante.

No todas las interfaces necesitan todas las variantes.

### 5.2. Campos de formulario

Permiten introducir información. Su diseño debe contemplar:

- Etiqueta.
- Campo de entrada.
- Ayuda, si es necesaria.
- Mensaje de validación o error.
- Indicación de obligatoriedad cuando corresponda.

Un placeholder no debería sustituir automáticamente a una etiqueta: el texto provisional puede desaparecer al escribir.

### 5.3. Tarjetas

Agrupan información relacionada. Pueden incluir título, descripción, imagen, metadatos y una acción.

Su estructura debe ser consistente cuando se utilizan para representar elementos equivalentes.

### 5.4. Navegación

Permite desplazarse entre secciones o páginas. Debe comunicar claramente el destino de cada opción y mantener una organización previsible.

### 5.5. Avisos y mensajes

Informan de situaciones como éxito, advertencia o error. Deben explicar qué ha ocurrido y, cuando proceda, qué puede hacer el usuario.

## 6. Patrones de interfaz

Un patrón es una solución recurrente a un problema de organización o interacción. Ejemplos:

- Barra de navegación.
- Formulario de acceso.
- Listado de tarjetas.
- Panel lateral.
- Ventana de confirmación.
- Buscador con resultados.

Un patrón combina componentes y reglas de composición. Por ejemplo, un formulario de acceso utiliza etiquetas, campos, botones y enlaces organizados para completar una tarea.

## 7. Describir un componente

Para documentar un componente, responde:

1. ¿Qué función tiene?
2. ¿Qué contenido muestra?
3. ¿Qué partes lo forman?
4. ¿Qué variantes necesita?
5. ¿Qué estados puede presentar?
6. ¿Dónde debe utilizarse?
7. ¿Qué errores de uso deben evitarse?

Ejemplo de ficha de botón:

| Propiedad | Definición |
|---|---|
| Nombre | Botón principal |
| Función | Ejecutar la acción prioritaria |
| Etiqueta | Verbo claro: «Guardar», «Continuar» |
| Variante | Principal |
| Estado | Normal, deshabilitado, en proceso |
| Uso | Una acción prioritaria por contexto, cuando sea posible |

## 8. Ejemplo guiado: catálogo de libros

Cada libro puede mostrarse mediante una tarjeta con:

- Título.
- Autor.
- Imagen de portada.
- Breve descripción.
- Acción «Consultar».

Todas las tarjetas mantienen el mismo orden y estilo. Si un libro no tiene imagen, se debe definir cómo se representa esa ausencia sin romper la composición.

## 9. Actividades

### Nivel 1. Fundamentos

**E16. Inventario de componentes**

Localiza en una web tres botones, dos campos, dos tarjetas y un elemento de navegación. Describe su función y contenido.

**Objetivo:** reconocer componentes en interfaces reales.

**Resultado esperado:** inventario organizado por tipo.

### Nivel 2. Aplicación

**E17. Fichas de componentes**

Diseña las fichas de un botón principal, un botón secundario, una tarjeta y un campo de formulario para una plataforma educativa.

**Objetivo:** documentar componentes reutilizables.

**Resultado esperado:** cuatro fichas con función, partes, variantes y reglas de uso.

### Nivel 3. Razonamiento

**E18. Reutilizar o crear otro componente**

Una aplicación utiliza tres estilos diferentes de botón para realizar la misma acción y un único estilo para acciones que tienen consecuencias muy distintas.

Explica qué problemas puede generar y cómo reorganizarías las variantes.

**Objetivo:** razonar sobre consistencia y significado.

**Resultado esperado:** propuesta de sistema de componentes justificada.

## 10. Reto: pequeño catálogo de componentes

Crea un catálogo visual para una aplicación de reservas. Incluye navegación, botones, tarjeta de actividad, campo de búsqueda y mensajes de estado. Todos deben compartir la misma identidad.

## 11. Errores frecuentes

- Diseñar componentes solo por apariencia.
- Utilizar etiquetas ambiguas como «Aceptar» cuando no se explica qué se acepta.
- Crear variantes sin una diferencia funcional.
- Cambiar el estilo de componentes equivalentes entre páginas.
- Olvidar estados de error o deshabilitado.
- Utilizar tarjetas para cualquier contenido aunque no aporten agrupación.

## 12. Buenas prácticas

- Diseña cada componente desde su función.
- Reutiliza soluciones coherentes.
- Define nombres y variantes.
- Documenta estados y contextos de uso.
- Mantén etiquetas claras.
- Comprueba el componente dentro de una pantalla real.

## 13. Resumen

Los componentes son unidades visuales y funcionales reutilizables. Los patrones combinan componentes para resolver tareas habituales. Documentar función, contenido, variantes y estados ayuda a mantener interfaces coherentes.

## 14. Autoevaluación

1. ¿Qué diferencia hay entre componente y patrón?
2. ¿Qué partes debería tener un campo?
3. ¿Por qué no debe dependerse siempre del placeholder?
4. ¿Qué información debe contener una ficha de componente?
5. ¿Por qué conviene limitar las variantes?

## 15. Checklist

- [ ] Identifico componentes comunes.
- [ ] Distingo componente y patrón.
- [ ] Describo su función además de su aspecto.
- [ ] Defino variantes y estados.
- [ ] Mantengo coherencia entre componentes equivalentes.
