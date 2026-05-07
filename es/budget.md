---
title: Presupuesto
parent: Español
nav_order: 2
---

> 🌐 Read this page in [English](../../en/budget/)

# Presupuesto

La página de Presupuesto es el corazón de savr. Es donde tomas decisiones en lugar de reaccionar a ellas.

Cada mes, tomas lo que tienes y le dices a cada dólar lo que va a hacer. Renta. Comida. Ahorros. Esa cita con el dentista que has estado posponiendo. Cuando terminas, cada dólar tiene un trabajo y sabes — con números reales, no con sensaciones — qué tienes disponible para qué.

Suena aburrido escrito así. En la práctica es sorprendentemente satisfactorio. Como organizar un clóset, pero con tu dinero.

---

## Anatomía de la página de presupuesto

| Elemento | Qué muestra |
|---|---|
| **Selector de mes / año** | Navega adelante o atrás por cualquier mes, pasado o futuro. Por defecto está el mes actual. |
| **Por presupuestar** | El número titular en la parte superior. Son ingresos que has recibido pero aún no tienen un trabajo. |
| **Saldo total de cuentas** | Suma de todas tus cuentas activas, mostrado junto al presupuesto como contexto. |
| **Grupos de categorías** | Agrupaciones colapsables. Cada grupo muestra métricas agregadas. |
| **Filas de categoría** | Cada categoría muestra Presupuestado, Gastado y Disponible para el mes seleccionado. |

Cada fila de categoría tiene tres números:

- **Presupuestado** — lo que has asignado este mes
- **Gastado** — lo que realmente has gastado en esta categoría este mes
- **Disponible** — `Presupuestado − Gastado`. El número que te importa.

Cuando **Disponible** se vuelve negativo, el valor se muestra en rojo. No es un regaño — es la señal de que debes mover dinero hacia ahí desde otra parte.

---

## Asignar dinero a las categorías

Haz clic en una categoría. Escribe cuánto quieres gastar ahí este mes. Guarda. Repite.

Cada asignación reduce **Por presupuestar** en la misma cantidad. La matemática que estás haciendo es muy simple:

> **Ingresos − Asignaciones = 0**

Cuando el lado derecho llega a cero, cada dólar tiene un trabajo y terminaste.

### Ejemplo trabajado

Empiezas el mes con $3,200 en tu cuenta corriente, todo ganado este mes. Por presupuestar muestra $3,200.

Empiezas a hacer clic en categorías:

| Categoría | Presupuestado | Por presupuestar después |
|---|---|---|
| Renta | $1,400 | $1,800 |
| Comida | $500 | $1,300 |
| Servicios | $150 | $1,150 |
| Teléfono e Internet | $120 | $1,030 |
| Gasolina | $180 | $850 |
| Restaurantes | $200 | $650 |
| Suscripciones | $40 | $610 |
| Fondo de Emergencia | $300 | $310 |
| Vacaciones | $200 | $110 |
| Hobbies | $110 | $0 |

Por presupuestar: $0. Mayo está completamente planeado. Puedes gastar con confianza porque cada dólar ya sabe para qué es.

### Cómo afectan los tipos de transacción a Por presupuestar

Cómo afectan las transacciones a Por presupuestar depende de su tipo:

| Tipo de transacción | Efecto en Por presupuestar |
|---|---|
| **Ingreso** | Aumenta Por presupuestar |
| **Gasto** | Sin efecto directo (reduce Disponible de la categoría vía Gastado) |
| **Crédito** | Sin efecto en Por presupuestar. Solo reduce el Gastado de la categoría. |
| **Transferencia** | Sin efecto — el dinero se mueve entre tus cuentas |

> **Por qué Crédito no se suma a Por presupuestar:** Un reembolso cancela un gasto previo. Si compraste $80 de comida y devolviste $20, tu categoría debe reflejar $60 de gasto neto — no "$80 gastados + $20 de ingreso nuevo para presupuestar." Crédito lo hace bien. Usa Ingreso para dinero realmente nuevo: sueldos, regalos, intereses ganados.

---

## Mover dinero entre categorías

Aquí está la idea clave que hace que el presupuesto sea soportable: **no tienes que ser perfecto**.

Vas a excederte en algo cada mes. Restaurantes es clásico — sales un par de veces y la categoría se pone en rojo. Eso no es un fracaso moral. Es información. La solución es un clic:

1. Haz clic en la categoría origen (la que tiene excedente).
2. Usa la acción **Mover dinero**.
3. Elige la categoría destino y el monto.
4. Guarda.

Ambas categorías ahora muestran la transferencia en su historial. Tu Por presupuestar general sigue en cero. Nada está roto — solo ajustaste el plan.

> **Escenario común:** Presupuestaste $200 para Restaurantes y terminaste en $245. Disponible es -$45. Mueves $45 desde Hobbies (donde apenas has gastado) hacia Restaurantes. Ambas categorías se rebalancean. Presupuesto total sin cambios.

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
> - Renta — Objetivo Mensual de $1,400, vence el día 1.
> - Comida — Objetivo Semanal de $125 (savr sabe que son ~$540/mes).
> - Seguro de auto — Objetivo Anual de $720, vence en octubre.
> - Vacaciones — Objetivo Personalizado de $2,400 para agosto del próximo año. savr sugiere ~$200/mes.

### Configurar un objetivo

1. Haz clic en una categoría para abrir su panel de detalle.
2. Haz clic en **Establecer objetivo**.
3. Elige el tipo y monto.
4. Para Personalizados, configura la fecha objetivo y (opcionalmente) intervalo de repetición.
5. Para Mensuales, opcionalmente activa **Arrastre** para que el saldo no usado pase al siguiente mes.

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
- **Desglose efectivo vs crédito** — gasto dividido entre cuentas tipo efectivo (cuenta corriente, ahorros, efectivo) y tarjetas de crédito. Útil cuando quieres saber "okay, ¿pero cuánto va a salir realmente de mi cuenta corriente este mes?"
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

- **Apunta a Por presupuestar = 0.** Cualquier cosa en Por presupuestar no tiene plan. Planéalo. Incluso "Cosas Futuras" es una categoría donde puedes estacionar dinero.
- **No presupuestes dinero que no tienes.** Solo lo que ya está en tus cuentas puede asignarse. Los ingresos futuros se presupuestan el mes que llegan.
- **Ajusta a mitad de mes sin culpa.** Sobregirar no es fracaso. Es información. Mueve dinero, sigue.
- **Usa los objetivos con calma al inicio.** Acostúmbrate a la asignación manual un par de meses. Configurarás mejores objetivos cuando conozcas tus números reales.
- **Revisa al cierre del mes.** Pasa dos minutos viendo categorías con excedente. Pásalo al siguiente mes, mándalo a ahorros, o muévelo a donde estás atrás. El dinero sobrante es un regalo a tu yo futuro — no lo desperdicies.
- **Las categorías aburridas también merecen amor.** Un objetivo mensual en la renta se siente inútil porque siempre la pagas. Pero hace que Llenar por Objetivos funcione sin pensar. Vale la pena.
