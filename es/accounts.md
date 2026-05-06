---
title: Cuentas
parent: Español
nav_order: 3
---

> 🌐 Read this page in [English](../en/accounts/)

# Cuentas

Las cuentas representan las cuentas financieras reales que quieres dar seguimiento en savr: cuentas bancarias, tarjetas de crédito, efectivo, cuentas de inversión y préstamos.

Cada transacción pertenece a una cuenta. Los saldos de las cuentas se actualizan automáticamente conforme registras actividad, así que los totales en savr siempre reflejan la realidad.

---

## Tipos de cuenta

savr soporta seis tipos de cuenta. Elegir el tipo correcto importa porque afecta cómo se agrupa la cuenta, cómo se interpreta su saldo y qué funciones aplican.

| Tipo | Úsalo para | Notas |
|---|---|---|
| **Cheques** | Gastos del día a día | Aquí vive la mayoría de las transacciones |
| **Ahorros** | Dinero apartado | Se trata como Cheques para fines de presupuesto |
| **Tarjeta de Crédito** | Tarjetas de crédito | Gastar aquí no reduce una cuenta de efectivo; usa Transferencia para registrar pagos |
| **Efectivo** | Efectivo en mano | Útil para llevar el control del dinero de bolsillo |
| **Inversión** | Brokerages, retiro, cripto | Sigue saldos; no está pensado para detalle por operación |
| **Préstamo** | Hipotecas, créditos automotrices, créditos personales, créditos educativos | Incluye tasa de interés, pago mensual y categoría de pago vinculada |

> Los préstamos son especiales — consulta [Cuentas de préstamo](#cuentas-de-préstamo) abajo.

---

## Agregar una cuenta

1. Abre **Cuentas** y haz clic en **Agregar Cuenta**.
2. Ingresa:
   - **Nombre** — cómo aparece la cuenta en todo savr (p. ej. "BBVA Cheques")
   - **Tipo** — elige uno de los seis
   - **Saldo inicial** — el saldo actual. savr lo usa para inicializar la cuenta.
3. Para préstamos, completa los campos específicos del préstamo (ver abajo).
4. Haz clic en **Guardar**.

savr crea automáticamente una transacción de **Saldo Inicial** igual al valor que ingresaste. Esta transacción está marcada de forma especial: establece el saldo de la cuenta pero no afecta tu presupuesto ni el gasto de las categorías.

---

## Cuentas de préstamo

Las cuentas de préstamo tienen campos y funciones extra para que puedas dar seguimiento al capital, los intereses y el avance con el tiempo.

Al crear o editar un préstamo, puedes configurar:

| Campo | Significado |
|---|---|
| **Tasa de interés** | Tasa anual en porcentaje. Se usa para reportes y pagos recurrentes de deuda. |
| **Pago mensual** | El pago periódico esperado. Se usa como valor por defecto al aplicar pagos recurrentes. |
| **Categoría de pago vinculada** | La categoría a la que se cargan los intereses y comisiones del préstamo cuando registras un pago. |

Al crear un préstamo, puedes vincularlo a una **categoría existente** o pedir a savr que **cree una categoría nueva** (y opcionalmente la coloque en un grupo nuevo, como "Deuda"). Esto mantiene los intereses visibles en tu presupuesto sin configuración manual.

Para registrar pagos de préstamo con desglose de capital, intereses y comisiones, consulta [Pagos de deuda](transactions/#pagos-de-deuda).

---

## Editar, cerrar, reabrir, eliminar

### Editar una cuenta

Haz clic en la fila de la cuenta para abrir su editor. Puedes cambiar el nombre, el tipo y (para préstamos) la tasa de interés y el pago mensual. El saldo inicial se establece al crear — para ajustar saldos históricos, edita o agrega una transacción.

### Cerrar una cuenta

Cuando termines de usar una cuenta pero quieras conservar su historial:

1. Abre la vista de detalle de la cuenta.
2. Haz clic en **Cerrar**.

Las cuentas cerradas se ocultan de la lista principal y no aparecen en los selectores de transacción, pero todas las transacciones se conservan. Es la opción correcta para tarjetas de crédito liquidadas, inversiones vendidas y cuentas que ya no usas.

### Reabrir una cuenta

En la sección de cuentas cerradas de la página Cuentas, haz clic en **Reabrir** para regresarla. Todo el historial se preserva.

### Eliminar una cuenta

Solo puedes eliminar una cuenta de forma permanente si no tiene transacciones más allá del saldo inicial. Si necesitas eliminar una cuenta con actividad, tienes dos opciones:

1. Eliminar o reasignar cada transacción primero, o
2. Cerrar la cuenta — al cerrar, se preserva el historial.

---

## Organizar la página de cuentas

### Agrupación por tipo

Las cuentas se agrupan automáticamente por tipo. Cada grupo (Cheques, Ahorros, Tarjeta de Crédito, etc.) tiene un encabezado que muestra el saldo total del tipo.

### Colapsar y expandir

Haz clic en cualquier encabezado de grupo para colapsarlo. Úsalo para enfocarte en las cuentas con las que estás trabajando activamente.

### Reordenar cuentas

savr permite arrastrar y soltar en dos niveles:

- **Dentro de un grupo** — arrastra cuentas individuales para cambiar su orden.
- **Entre grupos** — arrastra el encabezado del grupo para cambiar el orden de los tipos.

Tu orden se guarda automáticamente y persiste entre sesiones.

---

## Vista de detalle de la cuenta

Haz clic en el nombre de una cuenta para abrir su página de detalle. Verás:

- El saldo actual y los metadatos de la cuenta (tipo, saldo inicial, fecha de creación)
- Todas las transacciones de esta cuenta, con los mismos filtros disponibles en la página principal de Transacciones
- Un botón **Nueva Transacción** para registrar actividad directamente contra la cuenta

Es la forma más rápida de conciliar una cuenta contra un estado de cuenta.

---

## Saldos de cuenta explicados

Los saldos se almacenan con dos decimales de precisión. Cada vez que creas, actualizas o eliminas una transacción, el saldo de la cuenta afectada se recalcula de forma atómica — así que el número en la página de Cuentas siempre coincide con la suma de su actividad.

Las transferencias entre dos cuentas registran un par enlazado: un débito y un crédito. Ambas cuentas se actualizan juntas.

Para tarjetas de crédito, el saldo refleja lo que debes (un número positivo significa que hay un saldo pendiente). Cuando registras un pago, transfiere dinero desde una cuenta de cheques a la cuenta de tarjeta — el saldo de la tarjeta baja, el de cheques baja, y tu patrimonio neto general no cambia.
