---
title: Presupuesto
parent: Español
nav_order: 2
---

> 🌐 Read this page in [English](../en/budget/)

# Presupuesto

La página de Presupuesto es el corazón de savr. Cada mes decides cómo se gasta cada unidad de dinero antes de que salga de tu cuenta. Cuando el valor **Por Asignar** llega a cero, cada peso tiene un propósito.

---

## Anatomía de la página de presupuesto

| Elemento | Qué muestra |
|---|---|
| **Selector de mes / año** | Navega a cualquier mes pasado o futuro. Por defecto se selecciona el mes actual. |
| **Por Asignar** | Ingresos que has recibido pero aún no has asignado a una categoría. La meta es mantenerlo en cero. |
| **Saldo total de cuentas** | Suma de todos los saldos de tus cuentas activas, mostrado junto al presupuesto como contexto. |
| **Grupos de categorías** | Agrupaciones colapsables de categorías (p. ej. "Servicios", "Metas"). Cada grupo muestra métricas agregadas. |
| **Filas de categoría** | Cada categoría muestra Asignado, Gastado y Disponible para el mes seleccionado. |

Cada fila de categoría tiene tres valores centrales:

- **Asignado** — lo que has asignado este mes
- **Gastado** — total de transacciones en esta categoría este mes
- **Disponible** — `Asignado − Gastado`. Lo que aún puedes gastar.

Cuando **Disponible** es negativo, el valor se muestra en rojo. Es la señal para mover dinero hacia esa categoría.

---

## Asignar dinero a las categorías

Haz clic en cualquier categoría e ingresa la cantidad que quieres presupuestar para el mes. Cada asignación reduce **Por Asignar** en la misma cantidad.

El objetivo del mes es simple:

> **Ingresos − Asignaciones = 0**

Si te queda saldo en Por Asignar, no has planificado todo. Si Por Asignar se vuelve negativo, has asignado de más y necesitas reducir en algún lado.

### Clasificación de ingresos

Cómo afectan las transacciones a Por Asignar depende de su tipo:

| Tipo de transacción | Efecto en Por Asignar |
|---|---|
| **Ingreso** | Aumenta Por Asignar |
| **Gasto** | Sin efecto directo (reduce el Disponible de la categoría vía Gastado) |
| **Reembolso** | Sin efecto en Por Asignar. Solo reduce el Gastado de la categoría. |
| **Transferencia** | Sin efecto — el dinero se mueve entre tus cuentas |

Esto significa que un reembolso cancela correctamente una compra anterior en tu categoría, sin inflar tus ingresos del mes.

---

## Mover dinero entre categorías

Cuando una categoría está sobregirada y otra tiene excedente, no necesitas romper el presupuesto — solo mueves dinero.

1. Haz clic en la categoría origen en la lista del presupuesto.
2. Usa la acción **Mover dinero** y elige la categoría destino y el monto.
3. La transferencia se registra en el historial de presupuesto de ambas categorías.

Tu **Por Asignar** general permanece en cero. Solo cambia la asignación interna.

---

## Estrategias de auto-asignación

savr puede llenar tu presupuesto automáticamente. Abre el menú **Auto-Asignar** en la página de Presupuesto y elige una estrategia:

| Estrategia | Qué hace | Cuándo es útil |
|---|---|---|
| **Insuficiente** | Llena cada categoría hasta su objetivo (o hasta lo ya gastado si no hay objetivo). | La más común — deja cada categoría "cubierta". |
| **Asignado el mes anterior** | Copia las asignaciones del mes pasado. | Meses predecibles donde nada ha cambiado. |
| **Gastado el mes anterior** | Asigna a cada categoría lo que realmente se gastó el mes pasado. | Verificar el presupuesto contra el gasto real. |
| **Disponible Cero** | Agrega dinero a categorías donde Disponible es negativo, llevándolas de regreso a cero. | Solución rápida cuando hay sobregiros tarde en el mes. |
| **Asignado Cero** | Asigna a categorías que aún no tienen presupuesto este mes. | Empezar un mes nuevo desde cero. |

Puedes ver el total que asignará cada estrategia antes de aplicarla, y opcionalmente fijar un máximo a gastar.

### Llenar por Objetivos

El botón **Llenar por Objetivos** es un atajo de un clic: llena cada categoría que tenga objetivo con el monto sugerido para el mes actual. Las categorías sin objetivo no se modifican.

### Auto-asignación por categoría

También puedes auto-asignar una sola categoría desde su menú de acciones. savr usa el objetivo de la categoría — o su gasto previo — para sugerir un monto.

---

## Objetivos (metas)

Un objetivo le dice a savr cuánto quieres presupuestar para una categoría, para que pueda mostrarte un estado de un vistazo (en regla, insuficiente, sin asignar) y potenciar funciones como Llenar por Objetivos.

### Tipos de objetivo

| Tipo | Comportamiento |
|---|---|
| **Mensual** | Recurrente cada mes. Opcionalmente ligado a un día específico del mes. |
| **Semanal** | Se repite cada semana en el día elegido (domingo a sábado). |
| **Anual** | Se repite anualmente en un mes y día específicos. |
| **Personalizado** | Ahorrar un monto total para una fecha objetivo. Puede repetirse cada N meses / años, o ser único. |

### Configurar un objetivo

1. Haz clic en una categoría para abrir su panel de detalle.
2. Haz clic en **Establecer objetivo**.
3. Elige el tipo de objetivo y el monto.
4. Para objetivos Personalizados, configura la fecha objetivo y (opcionalmente) un intervalo de repetición.
5. Para objetivos Mensuales, opcionalmente activa **Acumular** para que el saldo no usado pase al siguiente mes.

### Estado

Cada categoría con objetivo muestra uno de tres estados:

- **OK** — el presupuesto cumple o supera el objetivo
- **Insuficiente** — el presupuesto es menor que el objetivo
- **Sin asignar** — no hay nada presupuestado este mes

### Eliminar un objetivo

Abre el modal de objetivo de la categoría y haz clic en **Eliminar objetivo**. La categoría se mantiene; solo se borra la meta.

---

## Panel de detalle de la categoría

Haz clic en cualquier categoría para abrir su panel de detalle. Verás:

- **Historial de presupuesto** — cada asignación y transferencia de dinero de esta categoría, de más antiguo a más reciente
- **Desglose efectivo vs crédito** — gasto dividido entre cuentas de tipo efectivo (cheques, ahorros, efectivo) y tarjetas de crédito. Útil para conciliar una categoría con el flujo real de efectivo.
- **Transacciones recientes** — vista rápida de la actividad que genera el valor Gastado
- **Estado del objetivo** — si hay objetivo configurado

### Entradas del historial de presupuesto

En el historial aparecen dos tipos de entradas:

| Tipo de entrada | Qué representa |
|---|---|
| **Asignación** | Dinero que asignaste directamente a esta categoría. |
| **Transferencia** | Dinero movido desde o hacia otra categoría. |

---

## Consejos para un presupuesto saludable

- **Apunta a Por Asignar = 0.** Cualquier cosa en Por Asignar es dinero sin plan. Asígnalo.
- **No presupuestes dinero que no tienes.** Solo lo que ya está en tus cuentas puede asignarse. Los ingresos futuros se presupuestan el mes siguiente.
- **Ajusta a mitad de mes.** Sobregirar no es un fracaso — es información. Mueve dinero desde una categoría flexible (p. ej. Entretenimiento) para cubrirlo.
- **Usa los objetivos con calma al inicio.** Familiarízate con la asignación manual antes de depender del auto-llenado.
- **Revisa al cierre del mes.** Una mirada rápida a las categorías con Disponible positivo te ayuda a decidir si lo dejas pasar al siguiente mes o lo reasignas.
