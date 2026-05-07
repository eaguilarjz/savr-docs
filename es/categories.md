---
title: Categorías
parent: Español
nav_order: 5
---

> {% include lang-globe.html %} Read this page in [English](../../en/categories/)

# Categorías

Las categorías son las cubetas donde pones tu dinero. Comida. Renta. El Fondo de Vacaciones. El "compré una cafetera elaborada, por favor no me juzguen" fund.

Cada transacción de Gasto y Crédito vive en una categoría, y cada categoría vive dentro de un grupo de categorías. Elegir el nivel de detalle correcto es una de esas habilidades silenciosas que convierten un presupuesto mediocre en uno útil.

---

## Por qué importan las categorías

Las categorías son la unidad con la que asignas dinero en la página de Presupuesto y la unidad sobre la que se suma el gasto. Elegir el nivel correcto de granularidad es un balance:

- **Muy pocas categorías** → no puedes ver realmente a dónde va el dinero. "Otros: $1,247" no es información.
- **Demasiadas** → el mantenimiento se vuelve una tarea, dejas de usar savr, vuelves a preguntarte a dónde se fue el dinero.

Un punto de partida sólido: una categoría por cada cuenta recurrente (renta, servicios, teléfono), una para cada gasto variable importante (comida, transporte, restaurantes), y unas cuantas para metas y calidad de vida. Como 15–25 en total. Ajusta con el tiempo.

Puedes renombrar, reordenar, ocultar o eliminar categorías en cualquier momento, así que no te angusties por dejar la estructura perfecta desde el inicio.

---

## Plantillas de categorías

Si estás empezando de cero y quieres una ventaja, el [asistente de configuración](../getting-started/#el-asistente-de-configuración) ofrece tres plantillas pre-armadas:

- **Simple** — 8 grupos, 1–2 categorías cada uno. El presupuesto mínimo viable.
- **Estándar** — 8 grupos, 3–4 categorías cada uno. Probablemente lo que quieres.
- **Detallada** — 8 grupos, 5–6 categorías cada uno. Para gente que disfruta el seguimiento granular.

Puedes editar, renombrar o eliminar cualquier cosa que cree la plantilla. La plantilla solo te ahorra mirar una página de Categorías vacía el día uno.

Si te saltaste el asistente o quieres empezar de nuevo, siempre puedes crear grupos y categorías manualmente.

---

## Grupos de categorías

Los grupos son la forma de organizar visualmente las categorías. Ejemplos:

- **Servicios y Renta** — Renta, Servicios, Teléfono, Internet
- **Variables** — Comida, Transporte, Restaurantes
- **Metas** — Fondo de Emergencia, Vacaciones, Auto Nuevo
- **Calidad de Vida** — Entretenimiento, Suscripciones, Hobbies

Los grupos son puramente organizativos. No afectan la matemática. Solo evitan que tus páginas de Presupuesto y Categorías se vean como una lista larga sin orden.

### Crear un grupo

1. Abre **Categorías**.
2. Haz clic en **Nuevo grupo**.
3. Escribe un nombre y guarda.

### Editar un grupo

Haz clic en el nombre del grupo para renombrarlo. También puedes ocultar un grupo desde el menú de **edición** — consulta [Ocultar](#ocultar-categorías-y-grupos) abajo.

### Reordenar grupos

Arrastra el encabezado de un grupo hacia arriba o abajo. El orden aplica en todos lados donde se muestran los grupos (Presupuesto, Categorías, selectores de transacción).

### Eliminar un grupo

Para eliminar un grupo, todas las categorías dentro deben eliminarse o moverse fuera primero. savr te avisará si el grupo aún contiene categorías.

---

## Categorías

### Crear una categoría

1. Abre **Categorías**.
2. Elige el grupo donde pertenece.
3. Haz clic en **Nueva categoría** dentro de ese grupo.
4. Escribe el nombre y guarda.

> **Pro tip:** Los nombres de categoría soportan emojis. Un 🛒 o 🏠 al inicio convierte una lista larga en algo que puedes escanear de un vistazo. Úsalo con calma — emoji en cada categoría es más caótico que encantador.

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

savr mueve cada transacción a la nueva categoría y luego elimina la antigua. Tu historial se mantiene intacto — no se pierde ningún dato de gasto, solo cambia de hogar.

> **Escenario común:** Tienes categorías separadas para "Café" y "Restaurantes" y te das cuenta de que en realidad no quieres seguirlas por separado. Eliminas "Café" y reasignas sus 47 transacciones a "Restaurantes". Listo. La categoría Café desaparece pero el gasto se preserva.

---

## Ocultar categorías y grupos

A veces una categoría ya no es relevante (una meta única que terminaste, un servicio que cancelaste), pero quieres conservar su historial. Ocúltala en lugar de eliminar:

1. Abre las acciones de la categoría y activa **Ocultar**.

Las categorías ocultas no aparecen en la página de Presupuesto, ni en los selectores de transacciones, ni en las estrategias de auto-asignación. Los datos se preservan. Muéstralas de nuevo cuando quieras.

Lo mismo aplica a grupos enteros.

Es la forma más limpia de retirar una categoría que ya cumplió su propósito sin perder el historial.

> **Por ejemplo:** Corriste un Fondo de Boda de 6 meses y ya te casaste. Oculta la categoría — el gasto se queda en tus registros, pero no satura la página de Presupuesto de este mes.

---

## Cómo interactúan el gasto y el presupuesto

Algunas cosas que vale saber sobre cómo se comportan las categorías:

- El **Gasto** en una categoría es la suma de transacciones de Gasto menos cualquier transacción de Crédito para el mes seleccionado.
- **Asignado** es lo que asignaste este mes — independiente del gasto.
- **Disponible** = Asignado − Gastado. Cuando es negativo, la categoría está sobregirada.
- Los **Objetivos** se pueden configurar en cualquier categoría para indicar cuánto quieres presupuestar. Potencian la auto-asignación y el atajo Llenar por Objetivos. Consulta [Presupuesto → Objetivos](../budget/#objetivos-también-llamados-metas).

Las categorías ocultas no aparecen en el presupuesto, pero siguen recibiendo las transacciones que ya les asignaste. Para dejar de registrar nuevas transacciones a una categoría, simplemente no la elijas al crearlas — o elimínala (con reasignación).

---

## Consejos

- **Empieza amplio.** Agrega detalle después si te encuentras queriendo dar seguimiento a algo específico. Una categoría "Cuidado Personal" que agrupa cortes de cabello, jabón y skincare está bien — hasta el día que realmente quieras saber cuánto gastaste en cortes de cabello. Ahí la divides.
- **Usa grupos para jerarquía, no categorías.** Es tentador hacer subcategorías como "Restaurantes → Comida" y "Restaurantes → Cena". No. Usa una sola categoría Restaurantes con notas en cada transacción. Mucho más fácil de mantener.
- **Una categoría por compromiso real.** Si tienes una cuenta mensual fija, dale su propia categoría. Un objetivo limpio en Renta funciona porque la renta es una sola cosa. Un objetivo en "Cuentas" lo enturbia.
- **Oculta antes de eliminar.** Ocultar es reversible. Eliminar (con reasignación) fusiona historial en otra categoría de forma permanente. En la duda, oculta.
- **Revisa tu lista de categorías cada seis meses.** Algunas se sentirán obvias de quitar. Otras se sentirán obvias de agregar. Tu gasto cambia — tus categorías deberían seguirle el paso.
