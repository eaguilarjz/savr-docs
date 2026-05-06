---
title: Recurrentes
parent: Español
nav_order: 6
---

> 🌐 Read this page in [English](../en/recurring/)

# Transacciones Recurrentes

Las transacciones recurrentes son plantillas que generan transacciones reales según un calendario. Úsalas para cualquier cosa predecible: sueldos, renta, suscripciones, pagos de préstamos, transferencias regulares a ahorros.

Cada regla recurrente lleva el control de cuándo debe ejecutarse la siguiente vez. Cuando llega esa fecha, savr puede aplicar la regla y crear una transacción real en la cuenta correspondiente.

---

## Frecuencias

Hay cinco frecuencias de recurrencia disponibles:

| Frecuencia | Descripción |
|---|---|
| **Diaria** | Cada día |
| **Semanal** | Cada 7 días |
| **Quincenal** | Cada 14 días — común para sueldos |
| **Mensual** | Mismo día cada mes |
| **Anual** | Mismo día cada año |

También puedes configurar una **fecha de fin** opcional para detener una recurrencia (útil para obligaciones finitas como un plan de cuotas o una suscripción de 12 meses).

---

## Crear una transacción recurrente

1. Abre **Recurrentes** y haz clic en **Nueva recurrente**.
2. Elige un **tipo**:
   - Ingreso — un sueldo regular u otro ingreso
   - Gasto — una cuenta recurrente, suscripción o cargo
   - Transferencia — movimiento automático entre dos de tus cuentas (p. ej. sueldo → ahorros)
   - Reembolso — devolución o rebaja recurrente
   - Pago de Deuda — pago de préstamo con desglose de capital/interés/comisiones
3. Configura el calendario:
   - **Frecuencia**
   - **Fecha de inicio** — primera ocurrencia
   - **Fecha de fin** (opcional) — detener después de esta fecha
4. Llena los detalles de la transacción:
   - **Cuenta** (y **cuenta destino** para Transferencia)
   - **Monto**
   - **Categoría** (o divisiones — ver abajo)
   - **Beneficiario** (opcional)
   - **Memo** (opcional)
5. Guarda.

La regla recurrente se guarda con una **siguiente fecha** igual a tu fecha de inicio. A partir de ahí, avanza cada vez que se aplica la regla.

---

## Divisiones en transacciones recurrentes

Las reglas recurrentes soportan la misma funcionalidad de divisiones que las transacciones puntuales. Activa **Dividir** en el editor de la recurrente y agrega filas para cada categoría. Las sumas de las divisiones deben coincidir con el monto de la regla.

Cuando se aplica la regla, la transacción resultante hereda las divisiones.

---

## Pagos de deuda recurrentes

Para pagos de préstamos, configura el tipo como **Pago de Deuda** y proporciona:

- **Cuenta origen** — de dónde sale el dinero (típicamente cheques)
- **Cuenta de préstamo** — el préstamo que se está pagando
- **Capital** — monto que reduce el saldo del préstamo
- **Interés** — monto registrado como gasto en la categoría de pago
- **Comisiones** — monto registrado como gasto en la categoría de pago

Cada vez que la regla se ejecuta, savr crea una entrada pareada que baja el saldo del préstamo por el capital y registra intereses y comisiones como gasto en la categoría vinculada.

Es la forma más limpia de dar seguimiento a un préstamo amortizado: la porción del capital crece automáticamente cada mes mientras los intereses suelen reducirse, y no tienes que recalcular el desglose manualmente.

---

## Aplicar transacciones vencidas

Una regla recurrente está **vencida** cuando su siguiente fecha es hoy o anterior. Hasta que se aplique la regla, no existe ninguna transacción real — solo la plantilla.

### Aplicar vencidas

1. Abre **Recurrentes**.
2. Las reglas vencidas aparecen al inicio con una acción de **Aplicar**.
3. Haz clic en **Aplicar vencidas** para ejecutar todas las reglas vencidas a la vez, o aplícalas individualmente.

Por cada regla aplicada, savr:

- Crea una transacción real con los detalles de la regla
- Sella la transacción con una referencia de regreso a la regla recurrente
- Avanza la siguiente fecha de la regla por un periodo

### ¿Por qué no es automático?

La aplicación es manual a propósito. Te da la oportunidad de revisar la entrada antes de que aterrice en el historial de tu cuenta — útil cuando un monto ha cambiado (subió la renta, una suscripción se renovó a un precio mayor) o quieres saltarte un mes.

Si una regla está vencida por varios periodos (p. ej. una regla semanal sin ejecutar por un mes), aplicarla una vez crea una transacción y avanza la siguiente fecha por un periodo. Aplícala repetidamente para ponerte al día.

---

## Editar y eliminar

### Editar una regla

Haz clic en cualquier regla recurrente para editarla. Puedes cambiar la frecuencia, las fechas, el monto, las divisiones o cualquiera de las cuentas y categorías vinculadas.

Editar la regla **no** cambia retroactivamente las transacciones que ya fueron creadas por aplicaciones anteriores. Para cambiar una transacción pasada, edítala directamente en la página de Transacciones.

### Eliminar una regla

Haz clic en **Eliminar** dentro del editor. Eliminar una regla recurrente **no** elimina las transacciones que se crearon a partir de ella — tu historial se mantiene intacto. Solo estás removiendo el calendario futuro.

---

## Consejos

- **Empieza con sueldos y renta.** Son predecibles y de alto impacto — automatizarlos te libera de copiarlos cada mes.
- **Configura las siguientes fechas con realismo.** Si tu sueldo siempre cae en viernes, elige el siguiente viernes como fecha de inicio para que la cadencia sea correcta.
- **Revisa antes de aplicar.** Usa Aplicar Vencidas como un punto de revisión, no como algo que olvidas. Las suscripciones suben; las rentas cambian; revisar cada ocurrencia lo detecta a tiempo.
- **Usa fechas de fin para obligaciones finitas.** Una membresía de gimnasio de 12 meses o un crédito automotriz de 36 meses puede tener fecha de fin, así la regla se retira sola.
- **Combina con objetivos.** Una categoría de gasto recurrente con un objetivo Mensual igual al monto recurrente es el equivalente en savr a "configúralo y olvídate".
