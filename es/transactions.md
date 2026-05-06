---
title: Transacciones
parent: Español
nav_order: 4
---

> 🌐 Read this page in [English](../en/transactions/)

# Transacciones

Las transacciones registran cada movimiento de dinero hacia y desde tus cuentas. Mueven todo lo demás en savr: saldos de cuenta, gasto de categorías y métricas de presupuesto.

Puedes administrar transacciones desde la página **Transacciones** o directamente desde la vista de detalle de cualquier cuenta.

---

## Tipos de transacción

savr soporta cuatro tipos de transacción. Elegir el correcto importa porque afecta tanto los saldos de cuenta como los cálculos del presupuesto.

| Tipo | Efecto en la cuenta | Efecto en el presupuesto |
|---|---|---|
| **Ingreso** | Agrega dinero a la cuenta | Aumenta **Por Asignar** |
| **Gasto** | Resta dinero de la cuenta | Aumenta el **Gastado** en la categoría elegida |
| **Transferencia** | Mueve dinero entre dos de tus cuentas | Sin efecto en el presupuesto — el dinero se queda dentro de tu patrimonio |
| **Reembolso** | Regresa dinero a la cuenta | **Reduce** el Gastado en la categoría elegida. **No** suma a Por Asignar. |

> **Por qué Reembolso e Ingreso son distintos:** Un reembolso cancela un gasto previo — tu categoría debe reflejar el costo neto, pero el reembolso no es un ingreso nuevo. Reembolso lo maneja correctamente. Usa Ingreso para dinero realmente nuevo: sueldos, regalos, intereses ganados.

---

## Crear una transacción

1. Abre **Transacciones** y haz clic en **Nueva Transacción** (o abre la página de detalle de una cuenta y usa el mismo botón ahí).
2. Llena:
   - **Tipo** — Ingreso, Gasto, Transferencia o Reembolso
   - **Cuenta** — qué cuenta afecta
   - **Monto** — siempre positivo; el tipo determina la dirección
   - **Fecha** — por defecto hoy
   - **Categoría** — requerida para Gasto y Reembolso
   - **Beneficiario** — opcional, pero útil para análisis de gasto
   - **Memo** — notas opcionales
   - **Conciliada** — actívalo si la transacción ya fue conciliada con tu estado de cuenta
3. Haz clic en **Guardar**.

### Transferencias

Para una Transferencia, se te pedirán tanto la cuenta **origen** como la cuenta **destino**. savr crea un par enlazado de transacciones — un débito y un crédito — que siempre se mueven juntas. Si editas o eliminas un lado, el otro le sigue.

---

## Divisiones

Una división te permite repartir una sola transacción entre varias categorías. Es especialmente útil para visitas al supermercado donde compras tanto comida como artículos de hogar, o cualquier compra que no encaje limpiamente en una sola categoría.

Para dividir una transacción:

1. En el diálogo de creación o edición, activa **Dividir**.
2. Agrega una fila de división por cada categoría. Cada fila tiene:
   - **Categoría**
   - **Monto**
   - **Memo** (opcional)
3. La suma de las divisiones debe coincidir con el monto total de la transacción.

Puedes tener tantas divisiones como necesites. Para quitar una división, elimina su fila — si solo queda una división, savr convierte la transacción de regreso a una transacción normal (no dividida).

---

## Pagos de deuda

Los pagos de deuda son un tipo especializado de transacción para registrar pagos contra una cuenta de préstamo. Te dan un desglose limpio de los tres componentes que un pago de préstamo suele incluir:

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

Tu saldo de cheques baja por el pago total, el saldo del préstamo baja por el capital, y los intereses más comisiones aparecen como gasto en la categoría de pago.

---

## Estado conciliado

Cada transacción tiene una bandera de **conciliada**. Úsala para marcar transacciones que ya han sido confirmadas por tu banco.

Flujos comunes:

- Concilia contra un estado de cuenta una vez al mes, marcando cada línea conforme avanzas.
- Deja las transacciones recientes sin conciliar hasta que se publiquen del lado del banco.

La bandera de conciliada es informativa — no cambia los cálculos de saldo.

---

## Editar y eliminar transacciones

Haz clic en cualquier transacción de la lista para abrir su diálogo de edición. Puedes cambiar cualquier campo, incluyendo convertir una transacción regular en dividida o viceversa. Haz clic en **Guardar** para aplicar.

Para eliminar una transacción, abre el diálogo de edición y haz clic en **Eliminar**. Las eliminaciones son permanentes y el saldo de la cuenta afectada se actualiza al instante.

> Las **transacciones de saldo inicial** son especiales. Se crean automáticamente con cada cuenta y no afectan los presupuestos. Puedes editar el monto si te equivocaste con tu saldo inicial, pero no puedes eliminar la entrada de saldo inicial sin eliminar la cuenta.

---

## Filtros

La página de Transacciones tiene una barra de filtros en la parte superior para encontrar actividad rápidamente:

| Filtro | Qué hace |
|---|---|
| **Cuenta** | Muestra las transacciones de una cuenta específica |
| **Categoría** | Muestra las transacciones de una categoría específica |
| **Beneficiario** | Muestra las transacciones de un beneficiario específico |
| **Tipo** | Restringe a Ingreso, Gasto, Transferencia o Reembolso |
| **Rango de fechas** | Elige una fecha de inicio y fin |

Los filtros se combinan con lógica **Y** — todas las restricciones aplican. Para limpiar filtros, presiona el botón de reinicio o quítalos uno a uno.

---

## Paginación

Las listas largas de transacciones se cargan en páginas de 50 a la vez. Conforme te acercas al final, savr trae el siguiente lote automáticamente. No hay botón de "siguiente página" — solo sigue desplazándote.

Para consultas muy grandes, puede ser mejor aplicar un filtro de rango de fechas en lugar de desplazarte por todo.

---

## Vínculos a transacciones recurrentes

Las transacciones creadas desde una [regla recurrente](recurring/) mantienen una referencia a la regla que las generó. Esto te permite rastrear una transacción hasta su plantilla y le permite a savr mantener tu calendario recurrente preciso.

Editar una transacción creada por una regla recurrente no cambia la regla misma — solo esa ocurrencia.

---

## Vista de detalle de la cuenta

Cada cuenta tiene una página de detalle que muestra la misma lista de transacciones, restringida a solo esa cuenta. Úsala para:

- Conciliar contra un estado de cuenta físico o en línea
- Agregar varias transacciones para una cuenta rápidamente
- Revisar la actividad en un periodo específico sin configurar filtros de cuenta
