---
title: Transacciones
parent: Español
nav_order: 4
---

> 🌐 Read this page in [English](../../en/transactions/)

# Transacciones

Las transacciones son los recibos de tu vida financiera. Cada peso que se mueve — entra, sale, o se mueve lateralmente entre tus cuentas — recibe una transacción.

savr usa las transacciones para mover todo lo demás: saldos de cuenta, gasto de categorías, el presupuesto, los reportes. Si las haces bien, el resto se cuida solo.

Puedes administrar transacciones desde la página **Transacciones** o directamente desde la vista de detalle de cualquier cuenta. Ambas funcionan igual.

---

## Los cuatro tipos de transacción

Elegir el tipo correcto importa. Aquí está la chuleta:

| Tipo | Efecto en la cuenta | Efecto en el presupuesto |
|---|---|---|
| **Ingreso** | Agrega dinero a la cuenta | Aumenta **Por Asignar** |
| **Gasto** | Resta dinero de la cuenta | Aumenta el **Gastado** en la categoría elegida |
| **Transferencia** | Mueve dinero entre dos de tus cuentas | Sin efecto — el dinero se queda dentro de tu patrimonio |
| **Reembolso** | Regresa dinero a la cuenta | **Reduce** el Gastado en la categoría. **No** suma a Por Asignar. |

> **Por qué Reembolso e Ingreso son distintos:** Un reembolso cancela un gasto previo. Tu categoría debe reflejar el costo neto (los $800 de la cuenta del super menos los $200 que devolviste), no "$800 gastados + $200 de ingreso nuevo para presupuestar." Reembolso lo hace bien. Usa Ingreso para dinero realmente nuevo: sueldos, regalos, intereses ganados.

### Ejemplos rápidos

| Hiciste esto | Usa este tipo |
|---|---|
| Te pagó tu empleador | Ingreso |
| Compraste comida | Gasto |
| Devolviste una camisa de $300 | Reembolso (contra tu categoría Ropa) |
| Pagaste la tarjeta de crédito desde cheques | Transferencia |
| Te llegó un cheque de $500 de cumpleaños de la abuela | Ingreso |
| Te reembolsaron un vuelo cancelado | Reembolso (contra tu categoría Viajes) |

---

## Crear una transacción

1. Abre **Transacciones** y haz clic en **Nueva Transacción** (o presiona el mismo botón en la página de detalle de una cuenta).
2. Llena:
   - **Tipo** — Ingreso, Gasto, Transferencia o Reembolso
   - **Cuenta** — qué cuenta afecta
   - **Monto** — siempre positivo; el tipo le dice a savr la dirección
   - **Fecha** — por defecto hoy
   - **Categoría** — requerida para Gasto y Reembolso
   - **Beneficiario** — opcional, pero útil para análisis de gasto
   - **Memo** — notas opcionales
   - **Conciliada** — actívalo si ya está conciliada con tu estado de cuenta
3. Haz clic en **Guardar**.

### Transferencias

Para una Transferencia, savr pide tanto la cuenta **origen** como la cuenta **destino**. Crea un par enlazado de transacciones — un débito y un crédito — que siempre se mueven juntas. Si editas una, la otra se actualiza. Si eliminas una, la otra se va también.

> **Por ejemplo:** Mueves $5,000 de Cheques a Ahorros. savr registra:
> - Cheques: -$5,000 (Transferencia a Ahorros)
> - Ahorros: +$5,000 (Transferencia desde Cheques)
> 
> Ambas transacciones comparten un emparejamiento interno. Tu patrimonio no cambia; el saldo de Cheques bajó, el de Ahorros subió.

---

## Divisiones

Una división te permite repartir una sola transacción entre varias categorías. Es el movimiento para visitas al supermercado donde compras tanto comida como artículos de hogar, o cualquier compra que no encaje limpiamente en una sola cubeta.

Para dividir:

1. En el diálogo de creación o edición, activa **Dividir**.
2. Agrega una fila por cada categoría, cada una con:
   - **Categoría**
   - **Monto**
   - **Memo** (opcional)
3. La suma de las divisiones debe coincidir con el monto total de la transacción.

> **Ejemplo trabajado:** Visita a Costco, $874.30 total. De eso, $540 fueron comida y $334.30 artículos de hogar (productos de limpieza, foco, esa cosa para el gato). Una transacción, dos divisiones, dos categorías. savr muestra el monto correcto en cada categoría.

Puedes tener tantas divisiones como necesites. Quita una división eliminando su fila — si solo queda una, savr convierte la transacción de regreso a una transacción normal (no dividida).

---

## Pagos de deuda

Los pagos de deuda son un tipo especializado de transacción para abonar a una cuenta de préstamo. Te dan un desglose limpio de los tres componentes que un pago de préstamo suele incluir:

| Componente | A dónde va |
|---|---|
| **Capital** | Reduce el saldo de la cuenta de préstamo |
| **Interés** | Se registra como gasto en la categoría de pago vinculada |
| **Comisiones** | Se registran como gasto en la categoría de pago vinculada |

Para registrar un pago de deuda:

1. Abre **Nueva Transacción** y cambia a modo **Pago de Deuda**.
2. Elige la **cuenta origen** (de dónde sale el dinero — usualmente cheques).
3. Elige la **cuenta de préstamo** que se está pagando.
4. Ingresa los montos de **capital**, **interés** y **comisiones**.
5. Confirma la categoría de pago (por defecto, la vinculada al préstamo).
6. Guarda.

Tu saldo de cheques baja por el pago total, el saldo del préstamo baja por el capital, y los intereses más comisiones aparecen como gasto en la categoría de pago. Sin matemática mental.

> **Ejemplo trabajado:** Tu pago hipotecario de $12,470 son $9,830 capital + $2,510 intereses + $130 comisiones. Registras el pago como Pago de Deuda:
> - Cheques: -$12,470
> - Saldo de la hipoteca: -$9,830
> - Categoría Intereses Hipoteca, Gastado: +$2,640 (intereses + comisiones)
> 
> El siguiente mes el capital sube un poquito y los intereses bajan. savr captura esto fielmente sin que rehagas la matemática.

Para pagos en calendario, consulta [Pagos de deuda recurrentes](../recurring/#pagos-de-deuda-recurrentes).

---

## Estado conciliada

Cada transacción tiene una bandera de **conciliada**. Es una forma simple de marcar transacciones confirmadas por tu banco — útil cuando estás haciendo coincidir tus registros con un estado de cuenta.

Dos flujos comunes:

- Concilia contra un estado de cuenta una vez al mes, marcando cada línea conforme avanzas. (El flujo de [Conciliación](../reconcile/) de savr lo hace automáticamente — recomendado.)
- Deja las transacciones recientes sin conciliar hasta que se publiquen del lado del banco.

La bandera de conciliada es solo informativa — no cambia los cálculos de saldo.

---

## Editar y eliminar transacciones

Haz clic en cualquier transacción de la lista para abrir su diálogo de edición. Puedes cambiar cualquier campo, incluyendo convertir una transacción regular en dividida o viceversa. Haz clic en **Guardar** para aplicar.

Para eliminar una transacción, abre el diálogo de edición y haz clic en **Eliminar**. Las eliminaciones son permanentes y el saldo de la cuenta afectada se actualiza al instante.

> **Atención:** Las **transacciones de saldo inicial** son especiales. Se crean automáticamente con cada cuenta y no afectan los presupuestos. Puedes editar el monto si te equivocaste con tu saldo inicial, pero no puedes eliminar la entrada de saldo inicial sin eliminar la cuenta.

---

## Filtros

La página de Transacciones tiene una barra de filtros en la parte superior para encontrar actividad rápido:

| Filtro | Qué hace |
|---|---|
| **Cuenta** | Muestra las transacciones de una cuenta específica |
| **Categoría** | Muestra las transacciones de una categoría específica |
| **Beneficiario** | Muestra las transacciones de un beneficiario específico |
| **Tipo** | Restringe a Ingreso, Gasto, Transferencia o Reembolso |
| **Rango de fechas** | Elige una fecha de inicio y fin |

Los filtros se combinan con lógica **Y** — todas las restricciones aplican. Para limpiar, presiona el botón de reinicio o quítalos uno a uno.

> **Por ejemplo:** ¿Quieres ver todo lo que gastaste en "Costco" este año? Filtra Beneficiario = Costco, Tipo = Gasto, Rango de fechas = enero 1 a hoy. Ahí está tu número.

---

## Paginación

Las listas largas de transacciones se cargan en páginas de 50. Conforme te acercas al final, savr trae el siguiente lote automáticamente. No hay botón de "siguiente página" — solo sigue desplazándote.

Para consultas muy grandes, configura un filtro de rango de fechas en lugar de desplazarte por todo.

---

## Vínculos a transacciones recurrentes

Las transacciones creadas desde una [regla recurrente](../recurring/) mantienen una referencia a la regla que las generó. Así que puedes rastrear cualquier transacción hasta su plantilla y savr puede mantener tu calendario recurrente preciso.

Editar una transacción creada por una regla recurrente no cambia la regla misma — solo esa ocurrencia. (¿Quieres cambiar la regla? Edítala directamente en la página de Recurrentes.)

---

## Importación masiva

¿Tienes un CSV de tu banco? No captures un año de transacciones a mano.

La página de [Importar y Exportar](../import-export/) cubre el asistente de importación CSV de tres pasos de savr, incluyendo cómo mapear columnas de cualquier formato de exportación bancaria y cómo evitar duplicados contra transacciones que ya capturaste.

---

## Vista de detalle de la cuenta

Cada cuenta tiene una página de detalle que muestra la misma lista de transacciones, restringida a solo esa cuenta. Úsala para:

- Conciliar contra un estado de cuenta físico o en línea (o haz clic en **Conciliar** para el flujo guiado)
- Agregar varias transacciones para una cuenta rápidamente
- Revisar la actividad en un periodo específico sin configurar filtros de cuenta

Es la misma página de Transacciones que ya conoces — solo más estrecha.
