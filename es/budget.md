---
title: Presupuesto
parent: Español
nav_order: 2
---

> 🌐 Read this page in [English](../../en/budget/)

# Presupuesto

La página de Presupuesto es el corazón de savr. Es donde tomas decisiones en lugar de reaccionar a ellas.

Cada mes, tomas lo que tienes y le dices a cada peso lo que va a hacer. Renta. Comida. Ahorros. Esa cita con el dentista que has estado posponiendo. Cuando terminas, cada peso tiene un trabajo y sabes — con números reales, no con sensaciones — qué tienes disponible para qué.

Suena aburrido escrito así. En la práctica es sorprendentemente satisfactorio. Como organizar un clóset, pero con tu dinero.

---

## Anatomía de la página de presupuesto

| Elemento | Qué muestra |
|---|---|
| **Selector de mes / año** | Navega adelante o atrás por cualquier mes, pasado o futuro. Por defecto está el mes actual. |
| **Por Asignar** | El número titular en la parte superior. Son ingresos que has recibido pero aún no tienen un trabajo. |
| **Saldo total de cuentas** | Suma de todas tus cuentas activas, mostrado junto al presupuesto como contexto. |
| **Grupos de categorías** | Agrupaciones colapsables. Cada grupo muestra métricas agregadas. |
| **Filas de categoría** | Cada categoría muestra Asignado, Gastado y Disponible para el mes seleccionado. |

Cada fila de categoría tiene tres números:

- **Asignado** — lo que has asignado este mes
- **Gastado** — lo que realmente has gastado en esta categoría este mes
- **Disponible** — `Asignado − Gastado`. El número que te importa.

Cuando **Disponible** se vuelve negativo, el valor se muestra en rojo. No es un regaño — es la señal de que debes mover dinero hacia ahí desde otra parte.

---

## Asignar dinero a las categorías

Haz clic en una categoría. Escribe cuánto quieres gastar ahí este mes. Guarda. Repite.

Cada asignación reduce **Por Asignar** en la misma cantidad. La matemática que estás haciendo es muy simple:

> **Ingresos − Asignaciones = 0**

Cuando el lado derecho llega a cero, cada peso tiene un trabajo y terminaste.

### Ejemplo trabajado

Empiezas el mes con $32,000 en tu cuenta de cheques, todo ganado este mes. Por Asignar muestra $32,000.

Empiezas a hacer clic en categorías:

| Categoría | Asignado | Por Asignar después |
|---|---|---|
| Renta | $14,000 | $18,000 |
| Comida | $5,000 | $13,000 |
| Servicios | $1,500 | $11,500 |
| Teléfono e Internet | $1,200 | $10,300 |
| Gasolina | $1,800 | $8,500 |
| Restaurantes | $2,000 | $6,500 |
| Suscripciones | $400 | $6,100 |
| Fondo de Emergencia | $3,000 | $3,100 |
| Vacaciones | $2,000 | $1,100 |
| Hobbies | $1,100 | $0 |

Por Asignar: $0. Mayo está completamente planeado. Puedes gastar con confianza porque cada peso ya sabe para qué es.

### Cómo afectan los tipos de transacción a Por Asignar

Cómo afectan las transacciones a Por Asignar depende de su tipo:

| Tipo de transacción | Efecto en Por Asignar |
|---|---|
| **Ingreso** | Aumenta Por Asignar |
| **Gasto** | Sin efecto directo (reduce Disponible de la categoría vía Gastado) |
| **Reembolso** | Sin efecto en Por Asignar. Solo reduce el Gastado de la categoría. |
| **Transferencia** | Sin efecto — el dinero se mueve entre tus cuentas |

> **Por qué Reembolso no se suma a Por Asignar:** Un reembolso cancela un gasto previo. Si compraste $800 de comida y devolviste $200, tu categoría debe reflejar $600 de gasto neto — no "$800 gastados + $200 de ingreso nuevo para presupuestar." Reembolso lo hace bien. Usa Ingreso para dinero realmente nuevo: sueldos, regalos, intereses ganados.

---

## Mover dinero entre categorías

Aquí está la idea clave que hace que el presupuesto sea soportable: **no tienes que ser perfecto**.

Vas a excederte en algo cada mes. Restaurantes es clásico — sales un par de veces y la categoría se pone en rojo. Eso no es un fracaso moral. Es información. La solución es un clic:

1. Haz clic en la categoría origen (la que tiene excedente).
2. Usa la acción **Mover dinero**.
3. Elige la categoría destino y el monto.
4. Guarda.

Ambas categorías ahora muestran la transferencia en su historial. Tu Por Asignar general sigue en cero. Nada está roto — solo ajustaste el plan.

> **Escenario común:** Presupuestaste $2,000 para Restaurantes y terminaste en $2,450. Disponible es -$450. Mueves $450 desde Hobbies (donde apenas has gastado) hacia Restaurantes. Ambas categorías se rebalancean. Presupuesto total sin cambios.

Este es el movimiento que evita que la gente abandone su presupuesto a mitad de mes. Acéptalo.

---

## Estrategias de auto-asignación

savr puede llenar tu presupuesto automáticamente. Abre el menú **Auto-Asignar** en la página de Presupuesto y elige una de cinco estrategias:

| Estrategia | Qué hace | Cuándo usarla |
|---|---|---|
| **Insuficiente** | Llena cada categoría hasta su objetivo (o hasta lo ya gastado si no hay objetivo). | La más común — deja cada categoría "cubierta." |
| **Asignado el mes anterior** | Copia las asignaciones del mes pasado tal cual. | Meses predecibles donde nada ha cambiado. |
| **Gastado el mes anterior** | Asigna a cada categoría lo que realmente se gastó el mes pasado. | Verificación de presupuesto contra hábitos reales. |
| **Disponible Cero** | Agrega dinero a categorías donde Disponible es negativo, llevándolas a cero. | Limpieza rápida a fin de mes cuando hay categorías rojas. |
| **Asignado Cero** | Asigna a categorías que aún no tienen presupuesto este mes. | Empezar un mes nuevo desde cero. |

Puedes ver el total que asignará cada estrategia antes de aplicarla, y opcionalmente fijar un máximo a gastar.

### Llenar por Objetivos

El botón **Llenar por Objetivos** es un atajo de un clic: financia cada categoría con objetivo con el monto sugerido para el mes actual. Las categorías sin objetivo no se tocan.

Este es el flujo "configúralo y olvídate" de la mayoría de la gente después de unos meses. Configura objetivos en tus categorías reales, haz clic en Llenar por Objetivos al inicio de cada mes, ajusta el resto manualmente.

### Auto-asignación por categoría

Cada categoría también tiene su propia acción de auto-asignación — útil cuando solo quieres llenar un lugar. savr sugiere un monto basado en el objetivo (o tu gasto previo si no hay objetivo).

---

## Objetivos (también llamados metas)

Un objetivo le dice a savr "esto es lo que quiero presupuestar para esta categoría." Una vez configurado, savr puede:

- Mostrarte un estado (en regla, insuficiente, sin asignar) de un vistazo
- Potenciar Llenar por Objetivos para financiar todo con un clic
- Sugerir montos en auto-asignación

### Tipos de objetivo

| Tipo | Comportamiento |
|---|---|
| **Mensual** | Se repite cada mes. Opcionalmente ligado a un día del mes. |
| **Semanal** | Se repite cada semana en un día específico (domingo a sábado). |
| **Anual** | Se repite anualmente en un mes + día específico. |
| **Personalizado** | Ahorrar un monto total para una fecha objetivo. Puede repetirse cada N meses / años, o ser único. |

> **Por ejemplo:**
> - Renta — Objetivo Mensual de $14,000, vence el día 1.
> - Comida — Objetivo Semanal de $1,250 (savr sabe que son ~$5,400/mes).
> - Seguro de auto — Objetivo Anual de $7,200, vence en octubre.
> - Vacaciones — Objetivo Personalizado de $24,000 para agosto del próximo año. savr sugiere ~$2,000/mes.

### Configurar un objetivo

1. Haz clic en una categoría para abrir su panel de detalle.
2. Haz clic en **Establecer objetivo**.
3. Elige el tipo y monto.
4. Para Personalizados, configura la fecha objetivo y (opcionalmente) intervalo de repetición.
5. Para Mensuales, opcionalmente activa **Acumular** para que el saldo no usado pase al siguiente mes.

### Estado del objetivo

Cada categoría con objetivo muestra uno de tres estados:

- **OK** — presupuestada al nivel del objetivo o más
- **Insuficiente** — presupuestada pero no lo suficiente
- **Sin asignar** — nada presupuestado este mes

### Eliminar un objetivo

Abre el modal de objetivo de la categoría y haz clic en **Eliminar objetivo**. La categoría se queda; solo se borra la meta.

> **Pro tip:** No pongas objetivos en cada categoría desde el principio. Empieza con las cuentas fijas aburridas (renta, servicios, suscripciones). Agrega objetivos a categorías variables solo después de observar tu gasto real un par de meses y tener números realistas.

---

## El panel de detalle de la categoría

Haz clic en cualquier categoría para abrir su panel de detalle. Verás:

- **Historial de presupuesto** — cada asignación y transferencia de dinero de esta categoría, del más antiguo al más reciente. La pista de auditoría de cómo llegó esta categoría a donde está hoy.
- **Desglose efectivo vs crédito** — gasto dividido entre cuentas tipo efectivo (cheques, ahorros, efectivo) y tarjetas de crédito. Útil cuando quieres saber "okay, ¿pero cuánto va a salir realmente de mi cuenta de cheques este mes?"
- **Transacciones recientes** — vista rápida de lo que está moviendo el valor Gastado
- **Estado del objetivo** — si hay objetivo configurado

### Entradas del historial de presupuesto

En el historial aparecen dos tipos de entradas:

| Tipo | Qué representa |
|---|---|
| **Asignación** | Dinero que asignaste directamente a esta categoría. |
| **Transferencia** | Dinero movido desde o hacia otra categoría. |

---

## Consejos de gente que sí hace esto

- **Apunta a Por Asignar = 0.** Cualquier cosa en Por Asignar no tiene plan. Planéalo. Incluso "Cosas Futuras" es una categoría donde puedes estacionar dinero.
- **No presupuestes dinero que no tienes.** Solo lo que ya está en tus cuentas puede asignarse. Los ingresos futuros se presupuestan el mes que llegan.
- **Ajusta a mitad de mes sin culpa.** Sobregirar no es fracaso. Es información. Mueve dinero, sigue.
- **Usa los objetivos con calma al inicio.** Acostúmbrate a la asignación manual un par de meses. Configurarás mejores objetivos cuando conozcas tus números reales.
- **Revisa al cierre del mes.** Pasa dos minutos viendo categorías con excedente. Pásalo al siguiente mes, mándalo a ahorros, o muévelo a donde estás atrás. El dinero sobrante es un regalo a tu yo futuro — no lo desperdicies.
- **Las categorías aburridas también merecen amor.** Un objetivo mensual en la renta se siente inútil porque siempre la pagas. Pero hace que Llenar por Objetivos funcione sin pensar. Vale la pena.
