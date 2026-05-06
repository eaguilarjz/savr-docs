---
title: Presupuesto
parent: Español
nav_order: 2
---

> 🌐 Read this page in [English](../en/budget/)

# Presupuesto

La página de Presupuesto es el corazón de savr. Cada mes decides cómo se gasta cada unidad de dinero antes de que salga de tu cuenta.

---

## El banner Por presupuestar

El banner **Por presupuestar (TBB)** está fijo en la parte superior de la página y siempre es visible mientras desplazas las categorías. Muestra:

- La cantidad de ingresos aún sin asignar
- Una frase rotatoria que cambia cada vez que el escenario cambia

| Escenario | Qué significa |
|---|---|
| Monto positivo | Tienes dinero esperando ser asignado a categorías |
| Cero | Cada unidad está contabilizada — presupuesto completo |
| Negativo (rojo) | Has asignado más de lo que tienes — reduce algunas categorías |

La frase usa el nombre de tu moneda configurada (ej. "Cada peso tiene un destino" o "Every US dollar has a job"), y hay 20 frases diferentes por escenario para que la experiencia se mantenga fresca.

---

## Leer la tabla de presupuesto

Las categorías están organizadas en grupos colapsables. Para cada categoría puedes ver:

| Columna | Qué muestra |
|---|---|
| Categoría | El nombre de la categoría (soporta emojis y unicode) |
| Presupuestado | Cuánto asignaste este mes |
| Gastado | El gasto real registrado hasta ahora |
| Disponible | Presupuestado + remanente − gastado |

### Barra de progreso

Cada fila de categoría tiene una **barra de progreso** directamente debajo del nombre. Te da una visualización instantánea de cuánto del saldo disponible se ha utilizado:

- **Verde oscuro** — saldo disponible sin gastar
- **Verde claro** — porción gastada (dentro del presupuesto)
- **Rojo / amarillo** — excedido

Una leyenda debajo de la barra siempre muestra las cifras exactas: cuánto se gastó, cuánto queda y si hay remanente del mes anterior.

---

## Asignar dinero

Haz clic en cualquier monto en la columna **Presupuestado** y escribe un nuevo valor.

- Presiona **Enter** para guardar
- Presiona **Escape** para cancelar sin hacer cambios
- Haz clic fuera para guardar

---

## El panel de detalle de categoría

Haz clic en cualquier **fila** de categoría para abrir el panel de detalle en el lado derecho de la pantalla. El panel permanece fijo mientras desplazas, siempre accesible.

### Desglose de estadísticas

| Estadística | Qué muestra |
|---|---|
| Remanente | Saldo no gastado transferido del mes anterior |
| Asignado este mes | El monto que presupuestaste para este mes |
| Gastos en efectivo | Gastos cargados a cuentas que no son de crédito |
| Gastos con crédito | Gastos cargados a tarjetas de crédito |
| **Disponible** | El saldo neto (remanente + asignado − gastos) |

Si la categoría está excedida, aparece una advertencia con el monto en números rojos.

### Estrategias de auto-asignación

El panel ofrece cinco estrategias para llenar esta categoría automáticamente:

| Estrategia | Qué hace |
|---|---|
| **Subcubierta** | Completa hasta el monto objetivo; nunca reduce lo ya asignado |
| **Asignado el mes pasado** | Copia el monto que asignaste el mes anterior |
| **Gastado el mes pasado** | Coincide con tu gasto real del mes pasado |
| **Disponible en cero** | Ajusta el presupuesto para que el saldo disponible llegue exactamente a cero (puede liberar remanente de vuelta al TBB) |
| **Presupuestado en cero** | Elimina todo el dinero asignado, dejando el presupuesto en cero |

Cada tarjeta de estrategia muestra una vista previa del cambio (+/−) antes de confirmar. Si no tienes suficiente dinero sin asignar (TBB), el monto se limita automáticamente y se muestra una advertencia. Haz clic en **Aplicar** para confirmar.

### Objetivo

El panel muestra el objetivo activo de la categoría junto con su estado (al día, subcubierto o sin cubrir). Haz clic en **Editar** para cambiarlo, o **Establecer objetivo** si aún no existe.

### Botones de acción

| Botón | Cuándo aparece | Qué hace |
|---|---|---|
| Cubrir exceso | La categoría está en números rojos | Abre el modal para tomar fondos de otra categoría |
| Mover dinero | El saldo disponible es positivo | Abre el modal para mover dinero |
| Ver transacciones | Siempre | Filtra la lista de transacciones a esta categoría del mes actual |
| Ver historial | Siempre | Muestra todas las asignaciones hechas a esta categoría este mes |

---

## Botones de acción rápida en las filas

Dos botones de ícono aparecen en cada fila de categoría al pasar el cursor:

- **⇄** — aparece cuando el saldo disponible es positivo; abre el diálogo para mover dinero
- **▼ (ícono de rellenar)** — aparece cuando la categoría está excedida; abre el diálogo para cubrir el exceso

Estos permiten actuar sin necesidad de abrir el panel de detalle.

---

## Mover dinero

1. Haz clic en **⇄** en una fila de categoría, o abre el panel de detalle y haz clic en **Mover dinero**.
2. Selecciona la categoría de destino.
3. Ingresa el monto a transferir.

### Cubrir exceso de gasto

Cuando una categoría se vuelve negativa, haz clic en el ícono de rellenar en la fila o en **Cubrir exceso** en el panel. Selecciona una categoría de origen para tomar los fondos.

---

## Objetivos

Un objetivo le indica a savr cuánto debe recibir una categoría cada período. Los objetivos impulsan el auto-llenado y muestran de un vistazo si una categoría está al día.

### Establecer un objetivo

Abre el panel de detalle de la categoría y haz clic en **Establecer objetivo** o **Editar** junto al objetivo existente. Elige un tipo:

| Tipo | Descripción |
|---|---|
| Mensual | Un monto fijo cada mes |
| Semanal | Monto × semanas en el mes |
| Anual | Total dividido en partes iguales en 12 meses |
| Personalizado | Un monto total específico para una fecha objetivo |

Activa **Remanente** si el dinero no gastado debe trasladarse al mes siguiente (útil para gastos irregulares o anuales).

---

## Auto-asignar (todas las categorías a la vez)

El botón **Auto-asignar** en la parte superior de la tabla llena todas las categorías simultáneamente. Elige una estrategia y savr limita cada categoría para que nunca superes tu saldo TBB.

### Llenar por objetivos

El botón **↓ Llenar por objetivos** llena todas las categorías que tienen un objetivo establecido, en un solo paso.

---

## Navegar entre meses

Usa las flechas **← →** en la parte superior para moverte entre meses, o haz clic en **Este mes** para regresar al mes actual. El banner TBB y la navegación de meses permanecen fijos mientras solo la tabla de categorías se desplaza.

Los meses pasados son de solo lectura — puedes revisar asignaciones y gastos pero no editarlos.

---

## Categorías y grupos ocultos

Las categorías ocultas son invisibles por defecto. Haz clic en **Mostrar ocultos** (aparece en la barra de navegación cuando existen elementos ocultos) para revelarlos temporalmente. Administra la visibilidad desde la página de **Categorías**.
