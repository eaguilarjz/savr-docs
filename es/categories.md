---
title: Categorías
parent: Español
nav_order: 5
---

> 🌐 Read this page in [English](../../en/categories/)

# Categorías

Las categorías te permiten agrupar tus gastos en cubetas con sentido para que la página de presupuesto se mantenga organizada y fácil de leer.

Cada transacción de Gasto y Reembolso se asigna a una categoría, y cada categoría vive dentro de un grupo de categorías. La agrupación es puramente organizativa — no afecta los cálculos.

---

## Por qué importan las categorías

Las categorías son la unidad con la que asignas dinero en la página de Presupuesto y la unidad sobre la que se suma el gasto. Elegir el nivel correcto de granularidad es un balance:

- **Muy pocas categorías** → no puedes ver realmente a dónde va el dinero.
- **Demasiadas** → el presupuesto se vuelve tedioso de mantener y dejas de usarlo.

Un punto de partida común: una categoría por cada cuenta recurrente (renta, servicios, teléfono), una para cada gasto variable importante (comida, transporte, restaurantes), y unas cuantas para metas y calidad de vida.

Puedes renombrar, reordenar, ocultar o eliminar categorías en cualquier momento, así que no te preocupes por dejar la estructura perfecta desde el inicio.

---

## Grupos de categorías

Los grupos son la forma de organizar visualmente las categorías. Ejemplos:

- **Servicios y Renta** — Renta, Servicios, Teléfono, Internet
- **Variables** — Comida, Transporte, Restaurantes
- **Metas** — Fondo de Emergencia, Vacaciones, Auto Nuevo
- **Calidad de Vida** — Entretenimiento, Suscripciones, Hobbies

### Crear un grupo

1. Abre **Categorías**.
2. Haz clic en **Nuevo grupo**.
3. Ingresa un nombre y guarda.

### Editar un grupo

Haz clic en el nombre del grupo para renombrarlo. También puedes ocultar un grupo desde el menú de **edición** — consulta [Ocultar](#ocultar-categorías-y-grupos) abajo.

### Reordenar grupos

Arrastra el encabezado de un grupo hacia arriba o abajo para cambiar su posición. El orden aplica en todos lados donde se muestran los grupos (Presupuesto, Categorías, selectores de transacción).

### Eliminar un grupo

Para eliminar un grupo, todas las categorías dentro deben ser eliminadas o movidas a otro grupo primero. savr te avisará si el grupo aún contiene categorías.

---

## Categorías

### Crear una categoría

1. Abre **Categorías**.
2. Elige el grupo donde pertenece la categoría.
3. Haz clic en **Nueva categoría** dentro de ese grupo.
4. Escribe el nombre y guarda.

> Los nombres de categoría soportan emojis. Un 🛒 o 🏠 al inicio es una forma rápida de escanear una lista larga.

### Editar una categoría

Haz clic en cualquier nombre de categoría para renombrarlo en línea. Presiona Enter para guardar, Escape para cancelar.

Para mover una categoría a otro grupo, arrástrala a la sección del grupo destino.

### Reordenar categorías

Arrastra categorías dentro de un grupo para cambiar su orden. El orden persiste entre sesiones y se refleja en la página de Presupuesto.

### Eliminar una categoría

Si la categoría no tiene transacciones, puedes eliminarla directamente.

Si la categoría **tiene transacciones**, savr abre un modal de **reasignación**:

1. Elige otra categoría que reciba todas las transacciones existentes.
2. Confirma.

savr mueve cada transacción a la nueva categoría y luego elimina la antigua. Esto mantiene tu historial intacto — no se pierde ningún dato de gasto.

---

## Ocultar categorías y grupos

A veces una categoría ya no es relevante (una meta única que terminaste, un servicio que cancelaste), pero quieres conservar su historial. En vez de eliminar:

1. Abre las acciones de la categoría y activa **Ocultar**.

Las categorías ocultas no aparecen en la página de Presupuesto, ni en los selectores de transacciones, ni en las estrategias de auto-asignación. Los datos se preservan y puedes mostrarlas de nuevo en cualquier momento. Lo mismo aplica a grupos enteros.

Es la forma más limpia de retirar una categoría que ya cumplió su propósito.

---

## Cómo interactúan el gasto y el presupuesto

Algunas cosas que vale saber sobre cómo se comportan las categorías:

- El **Gasto** en una categoría es la suma de transacciones de Gasto menos cualquier transacción de Reembolso para el mes seleccionado.
- **Asignado** es el monto que asignaste este mes — independiente del gasto.
- **Disponible** = Asignado − Gastado. Cuando es negativo, la categoría está sobregirada.
- Los **Objetivos** se pueden configurar en cualquier categoría para indicar cuánto quieres presupuestar. Los objetivos potencian la auto-asignación y el atajo Llenar por Objetivos. Consulta [Presupuesto → Objetivos](../budget/#objetivos-metas).

Las categorías ocultas no aparecen en el presupuesto, pero siguen recibiendo las transacciones que ya les asignaste. Para dejar de registrar nuevas transacciones a una categoría, simplemente no la elijas al crearlas — o elimínala (con reasignación).

---

## Consejos

- **Empieza con categorías amplias.** Agrega detalle después si te encuentras queriendo dar seguimiento a algo específico.
- **Usa grupos para jerarquía, no categorías.** Es tentador hacer subcategorías como "Restaurantes → Comida" y "Restaurantes → Cena" — pero una sola categoría "Restaurantes" con notas en cada transacción suele ser suficiente.
- **Una categoría por compromiso real del presupuesto.** Si tienes una cuenta mensual fija, dale su propia categoría para que un objetivo pueda darle seguimiento limpiamente.
- **Oculta en lugar de eliminar** si no estás seguro. Ocultar es reversible; eliminar (con reasignación) fusiona el historial en otra categoría de forma permanente.
