---
title: Recurrentes
parent: Español
nav_order: 6
---

> 🌐 Read this page in [English](../../en/recurring/)

# Transacciones Recurrentes

La mayor parte de tu vida financiera son repeticiones. Renta el día 1. Spotify el día 12. Sueldo cada quince días. Las transacciones recurrentes son plantillas que se ejecutan en un calendario, así no recapturas las mismas cosas 50 veces al año.

Cada regla recurrente lleva el control de cuándo debe ejecutarse la siguiente vez. Cuando llega el día, savr está lista para aplicar la regla y crear una transacción real en la cuenta correspondiente.

---

## Frecuencias

Cinco opciones de recurrencia:

| Frecuencia | Descripción |
|---|---|
| **Diaria** | Cada día |
| **Semanal** | Cada 7 días |
| **Quincenal** | Cada 14 días — la cadencia clásica del sueldo |
| **Mensual** | Mismo día cada mes |
| **Anual** | Mismo día cada año |

También puedes configurar una **fecha de fin** opcional para detener una recurrencia (útil para obligaciones finitas como un plan de cuotas a 12 meses o una suscripción anual).

---

## Crear una transacción recurrente

1. Abre **Recurrentes** y haz clic en **Nueva recurrente**.
2. Elige un **tipo**:
   - **Ingreso** — sueldo, regalía recurrente, esa transferencia regular de tu roomie
   - **Gasto** — cuenta recurrente, suscripción, membresía del gimnasio
   - **Transferencia** — movimiento automático entre dos de tus cuentas (p. ej. sueldo → ahorros)
   - **Reembolso** — devolución o rebaja recurrente
   - **Pago de Deuda** — pago de préstamo con desglose de capital/interés/comisiones
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

La regla se guarda con una **siguiente fecha** igual a tu fecha de inicio. A partir de ahí, avanza cada vez que se ejecuta.

> **Ejemplo trabajado — tu sueldo:** Te pagan quincenalmente los viernes, $2,400 netos. Configura:
> - Tipo: Ingreso
> - Frecuencia: Quincenal
> - Fecha de inicio: este viernes
> - Cuenta: Cheques
> - Monto: $2,400
> - Beneficiario: Acme Corp Nómina
> 
> A partir de ahora, cada quince días el viernes verás "Aplicar" junto a esta regla. Un clic y el ingreso aterriza en tu cuenta, listo para presupuestar.

---

## Divisiones en transacciones recurrentes

Las reglas recurrentes soportan divisiones, igual que las transacciones puntuales. Activa **Dividir** en el editor y agrega una fila por cada categoría. Las sumas de las divisiones deben coincidir con el monto de la regla.

Cuando la regla se ejecuta, la transacción resultante hereda las divisiones.

> **Por ejemplo:** Tu sueldo tiene $1,800 a cuenta de cheques y $600 yendo a una sub-cuenta de ahorros. Configuras la regla de ingreso con dos divisiones — $1,800 a "Sueldo → Cheques" y $600 a "Sueldo → Ahorros." Cada periodo de pago, ambos aterrizan en sus lugares correctos.

---

## Pagos de deuda recurrentes

Para pagos de préstamos, configura el tipo como **Pago de Deuda** y proporciona:

- **Cuenta origen** — de dónde sale el dinero (típicamente Cheques)
- **Cuenta de préstamo** — el préstamo que se está pagando
- **Capital** — monto que reduce el saldo del préstamo
- **Interés** — monto registrado como gasto en la categoría de pago
- **Comisiones** — monto registrado como gasto en la categoría de pago

Cada vez que la regla se ejecuta, savr crea una entrada pareada que baja el saldo del préstamo por el capital y registra intereses + comisiones como gasto en la categoría vinculada.

Es la forma más limpia de seguir un préstamo amortizado. La porción del capital crece automáticamente cada mes, los intereses suelen reducirse, y no tienes que recalcular el desglose manualmente. Configúralo una vez, aplícalo cada mes, observa el saldo del préstamo encaminarse a cero.

> **Ejemplo trabajado — tu hipoteca:** Tu pago hipotecario de $1,247 son aproximadamente $983 capital + $251 intereses + $13 comisiones. Configura una regla Mensual de Pago de Deuda con esos números. Aplícala cada mes. A lo largo de un año, puedes actualizar el reparto capital/interés un par de veces para alinearlo con la tabla de amortización del banco. Observa el saldo de la hipoteca encogerse y siente algo cercano a la felicidad.

---

## Aplicar transacciones vencidas

Una regla está **vencida** cuando su siguiente fecha es hoy o anterior. Hasta que la apliques, no existe ninguna transacción real — solo la plantilla.

### Aplicar vencidas

1. Abre **Recurrentes**.
2. Las reglas vencidas aparecen al inicio con una acción **Aplicar**.
3. Haz clic en **Aplicar vencidas** para ejecutar todas a la vez, o aplícalas individualmente.

Por cada regla aplicada, savr:

- Crea una transacción real con los detalles de la regla
- Sella la transacción con una referencia de regreso a la regla recurrente
- Avanza la siguiente fecha de la regla por un periodo

### ¿Por qué no es automático?

La aplicación es manual a propósito. Te da la oportunidad de revisar la entrada antes de que aterrice en el historial de tu cuenta. Esto importa porque:

- Las suscripciones suben de precio ("Spotify acaba de subirme de $10 a $12")
- Las rentas cambian
- Un cargo "mensual" del gimnasio a veces se salta un mes
- Quieres ver la transacción recurrente *antes* de que afecte tu saldo, no después

Si una regla está vencida por varios periodos (una semanal sin ejecutar por un mes), aplicarla una vez crea una transacción y avanza la siguiente fecha por un periodo. Aplícala repetidamente para ponerte al día — obtendrás la cantidad correcta de transacciones para la cantidad correcta de periodos.

> **Pro tip:** Haz que revisar la página de Recurrentes sea un ritual semanal. Dos minutos el domingo en la noche para aplicar lo que esté vencido. Tus transacciones se mantienen al día, las conciliaciones bancarias se hacen más fáciles, y atrapas los aumentos de precio el día que pasan.

---

## Editar y eliminar

### Editar una regla

Haz clic en cualquier regla recurrente para editarla. Puedes cambiar la frecuencia, las fechas, el monto, las divisiones o cualquiera de las cuentas y categorías vinculadas.

Editar la regla **no** cambia retroactivamente las transacciones que ya fueron creadas por aplicaciones anteriores. Para cambiar una transacción pasada, edítala directamente en la página de Transacciones.

### Eliminar una regla

Haz clic en **Eliminar** dentro del editor. Eliminar una regla recurrente **no** elimina las transacciones creadas a partir de ella — tu historial se mantiene intacto. Solo estás removiendo el calendario futuro.

> **Escenario común:** Cancelas ese servicio de streaming. Edita la fecha de fin de la regla a hoy, o simplemente elimina la regla. Las 14 transacciones mensuales que ya registraste se quedan en tu historial. El futuro se detiene.

---

## Consejos

- **Empieza con sueldos y renta.** Son predecibles y de alto impacto. Automatizarlos te libera de dos a cinco minutos al mes y hace que el resto se sienta más fácil.
- **Configura las siguientes fechas con realismo.** Si tu sueldo siempre cae en viernes, elige el siguiente viernes como fecha de inicio para que la cadencia sea correcta desde el día uno.
- **Revisa antes de aplicar.** Usa Aplicar Vencidas como un punto de revisión, no como algo que olvidas. La revisión de dos segundos atrapa los aumentos de precio que todos los demás no notan por seis meses.
- **Usa fechas de fin para obligaciones finitas.** Una membresía de gimnasio de 12 meses, un crédito automotriz de 36 meses — configura la fecha de fin y la regla se retira sola cuando deba.
- **Combina con objetivos.** Una categoría de gasto recurrente con un objetivo Mensual igual al monto recurrente es el equivalente en savr a "configúralo y olvídate."
- **Está bien saltar.** Si una regla está vencida pero no te cobraron este mes (el gimnasio cerró por remodelación, tu roomie olvidó mandarte la renta), no la apliques. Avanza manualmente la siguiente fecha en su lugar.
