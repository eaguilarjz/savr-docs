---
title: Conciliación
parent: Español
nav_order: 9
---

> {% include lang-globe.html %} Read this page in [English](../../en/reconcile/)

# Conciliación

Conciliar es el acto de decir: "el registro de savr de esta cuenta coincide con la realidad."

Tomas tu extracto del banco (o el "saldo actual" en línea de tu banco), lo comparas con lo que savr cree que debería ser el saldo y resuelves cualquier diferencia. Cuando los números cuadran, marcas como conciliado y sigues con tu vida.

Si nunca has conciliado — no te intimides. savr hace casi todo el trabajo. Tú solo estás haciendo clic en casillas hasta que dos números coincidan.

---

## Por qué conciliar

Tres razones:

1. **Atrapar tus propios errores de captura.** Escribiste $51 en lugar de $15. Pasa. La conciliación los saca a la luz en el momento que rompen la matemática.
2. **Atrapar errores del banco.** Raros pero reales. Un cargo duplicado, un crédito olvidado, una comisión que no sabías — aparecen cuando el número de savr difiere del banco.
3. **Construir confianza en tus propios datos.** Cuando el saldo en savr es el saldo real de tu cuenta, dejas de hedgear tus decisiones con "bueno, más o menos."

La recompensa por gastar dos minutos al mes por cuenta es confianza total en cada número que ves en savr.

---

## Cómo conciliar

1. Abre la página **Cuentas** y haz clic en la cuenta que quieres conciliar.
2. En la página de detalle, haz clic en **Conciliar**.
3. Estás en la página de conciliación. Tres cosas que hacer:

### Paso 1 — Ingresa el extracto

Arriba:

- **Fecha del extracto** — la fecha en el extracto del banco (o solo hoy, si usas el saldo en línea en tiempo real)
- **Saldo del extracto** — el saldo que el banco dice que tenía la cuenta en esa fecha

Ingresa ambos. savr los guarda cuando termines.

### Paso 2 — Concilia las transacciones que coinciden

Abajo, savr muestra una tabla de cada transacción no conciliada de la cuenta. Haz clic en filas (o usa las casillas) para marcar cuáles aparecen en el extracto.

Mientras haces clic, tres números se actualizan en la parte inferior de la página:

| Número | Qué es |
|---|---|
| **Saldo Conciliado** | Lo que savr cree que debería ser tu saldo después de todas las transacciones que marcaste |
| **Saldo del Estado de Cuenta** | Lo que escribiste arriba |
| **Diferencia** | Saldo del Estado de Cuenta − Saldo Conciliado |

Cuando **Diferencia = $0** (o dentro de medio centavo), el botón **Finalizar** se activa.

### Paso 3 — Finalizar

Haz clic en **Finalizar**. savr:

- Marca cada transacción seleccionada como conciliada y conciliada
- Registra la fecha y saldo del extracto
- Te regresa a la página de detalle de la cuenta

Listo. La cuenta está conciliada.

---

## ¿Y si no cuadra?

Esta es la parte que hace que conciliar parezca aterrador. Es realmente la parte donde se gana su lugar.

Si la **Diferencia** no es cero, algo está mal. O:

- Una transacción está en tu extracto pero no en savr (transacción faltante)
- Una transacción está en savr pero no en el extracto (transacción extra, o cuenta equivocada)
- Una transacción tiene el monto equivocado en algún lado

savr no auto-sugiere dónde está el problema — eso solo tú puedes resolverlo, porque depende de qué hay en tu extracto. Pero aquí está el flujo:

1. **Mira el tamaño de la diferencia.** Si son $43.21, probablemente buscas una sola transacción de $43.21.
2. **Escanea tu extracto por transacciones que no marcaste.** ¿Algo en el extracto pero no en tu pantalla? Esa es la transacción faltante. Agrégala (abre una nueva pestaña y usa la página de Transacciones) y regresa.
3. **Escanea tus transacciones marcadas por las que no estén en el extracto.** ¿Algo marcado pero no en el extracto? O no se ha publicado todavía (desmárcala e intenta de nuevo el siguiente mes) o no pertenece aquí (elimínala o corrígela).
4. **Vigila errores de signo y de monto.** Un cargo de $51 capturado como $15 producirá una diferencia de $36. Un débito capturado como crédito producirá una diferencia de dos veces el monto (porque está mal por -$X y +$X).

> **Escenario común:** Esperabas que la conciliación cuadrara y está a $25 de diferencia. Mirando el extracto, ves un retiro de cajero de $25 que olvidaste capturar. Abres una nueva pestaña, agregas la transacción, regresas a la página de conciliación (estará ahí esperando), marcas la transacción nueva, y la diferencia llega a cero. Haces clic en Finalizar.

---

## Qué tan seguido conciliar

Dos cadencias razonables:

- **Mensual**, contra el extracto oficial del banco. A la antigua pero sólido. El extracto es autoritativo.
- **Semanal o quincenal**, contra el "saldo actual" en línea del banco. Retroalimentación más rápida, menos transacciones por sesión, problemas más pequeños si algo está mal.

Elige la que sí vayas a hacer. Un hábito mensual que mantienes le gana a uno semanal que no.

> **Pro tip:** Configura un recordatorio de calendario recurrente para el día después de que termine tu periodo de extracto. "Conciliar cuenta corriente" — máximo cinco minutos. Tu yo futuro se lo agradecerá a tu yo presente.

---

## Conciliando tipos específicos de cuenta

### Cuenta corriente y ahorros

El pan y mantequilla de la conciliación. Hazla mensualmente contra el extracto. La mayoría de los meses cuadra al primer intento en menos de cinco minutos.

### Tarjetas de crédito

Mismo flujo que cuenta corriente. Nota que el saldo de una tarjeta de crédito es lo que debes (un número positivo). El saldo del extracto de la tarjeta es lo que te están facturando por ese periodo — que puede no coincidir con tu saldo actual, ya que has seguido gastando después de la fecha del extracto. Coincide contra el saldo del extracto para el periodo que cubre, ignorando transacciones después de esa fecha.

### Efectivo

El efectivo es difícil de conciliar porque no hay extracto. Mejor práctica: cuenta el efectivo en tu cartera, ingresa eso como el saldo del extracto y marca todas las transacciones que están en savr. Si no cuadra, olvidaste registrar un café por ahí. Agrégalo, finaliza, sigue.

### Cuentas de inversión

Los saldos de inversión se mueven diariamente con el valor de mercado. Conciliarlos contra un extracto es principalmente confirmar depósitos y retiros — los cambios impulsados por mercado son complicados de capturar transacción por transacción. Mucha gente solo actualiza el saldo inicial cada trimestre y no se molesta con conciliación completa.

### Préstamos

Los préstamos típicamente tienen una sola transacción al mes (el pago) más acumulación de intereses. Si usas transacciones de [pago de deuda](../transactions/#pagos-de-deuda), el saldo debería seguir el extracto del prestamista de cerca. Concilia cuando el prestamista mande un extracto de fin de año, o cuando los números se sientan raros.

---

## Historial de conciliación

Cada conciliación se registra contra la cuenta, incluyendo la fecha del extracto, el saldo y qué transacciones se marcaron. Las conciliaciones futuras se construyen encima — el "saldo previo del extracto" mostrado en la página de conciliación es la última terminada.

No necesitas mirar el historial seguido. Solo está ahí para el registro.

---

## Consejos

- **Concilia una cuenta a la vez.** No intentes conciliar cuenta corriente y ahorros al mismo tiempo — termina una antes de empezar la otra.
- **No fuerces un cuadre.** Si la diferencia es $0.34 y no la encuentras, no des clic en Finalizar de todas formas. El flujo de conciliación ni siquiera te dejará (Finalizar está deshabilitado hasta que la diferencia sea cero) — y eso es una característica. Encuentra el problema real. Casi siempre es una transacción real que necesita agregarse o corregirse.
- **Una conciliación fallida es información.** Si no puedes llegar a cero, savr te está diciendo "tus registros y la realidad están desincronizados en algún lado." Ese es un problema que vale la pena arreglar ahora, no ignorar.
- **La primera vez es la más difícil.** Si estás empezando una conciliación en una cuenta que no se ha conciliado en un año, tomará más de cinco minutos. Es normal. Después de la primera, es rápido.
