---
title: Actividad
parent: Español
nav_order: 4
redirect_from:
  - /es/transactions/
  - /es/transacciones/
---

> {% include lang-globe.html %} Read this page in [English](../../en/activity/)

# Actividad

Tu página de **Actividad** es el registro de tu vida financiera. Cada dólar que se mueve — entra, sale, o se mueve lateralmente entre tus cuentas — recibe una entrada aquí.

savr usa estas entradas para mover todo lo demás: saldos de cuenta, gasto de categorías, el presupuesto, los informes. Si las haces bien, el resto se cuida solo.

Puedes administrar la actividad desde la página **Actividad** o directamente desde la vista de detalle de cualquier cuenta. Ambas funcionan igual.

---

## Los cuatro tipos de transacción

Elegir el tipo correcto importa. Aquí está la chuleta:

| Tipo | Efecto en la cuenta | Efecto en el presupuesto |
|---|---|---|
| **Ingreso** | Agrega dinero a la cuenta | Aumenta **Por asignar** |
| **Gasto** | Resta dinero de la cuenta | Aumenta el **Gastado** en la categoría elegida |
| **Transferencia** | Mueve dinero entre dos de tus cuentas | Sin efecto — el dinero se queda dentro de tu patrimonio |
| **Crédito** | Regresa dinero a la cuenta | **Reduce** el Gastado en la categoría. **No** suma a Por asignar. |

> **Por qué Crédito e Ingreso son distintos:** Un reembolso cancela un gasto previo. Tu categoría debe reflejar el costo neto (los $80 de la cuenta del super menos los $20 que devolviste), no "$80 gastados + $20 de ingreso nuevo para presupuestar." Crédito lo hace bien. Usa Ingreso para dinero realmente nuevo: sueldos, regalos, intereses ganados.

### Ejemplos rápidos

| Hiciste esto | Usa este tipo |
|---|---|
| Te pagó tu empleador | Ingreso |
| Compraste comida | Gasto |
| Devolviste una camisa de $30 | Crédito (contra tu categoría Ropa) |
| Pagaste la tarjeta de crédito desde cuenta corriente | Transferencia |
| Te llegó un cheque de $50 de cumpleaños de la abuela | Ingreso |
| Te reembolsaron un vuelo cancelado | Crédito (contra tu categoría Viajes) |

---

## Crear una transacción

1. Abre **Actividad** y haz clic en **Nueva Transacción** (o presiona el mismo botón en la página de detalle de una cuenta).
2. Llena:
   - **Tipo** — Ingreso, Gasto, Transferencia o Crédito
   - **Cuenta** — qué cuenta afecta
   - **Monto** — siempre positivo; el tipo le dice a savr la dirección. **Puedes escribir expresiones matemáticas** aquí: `30+12.50`, `100/4`, `(15+8)*2` — savr las evalúa cuando sales del campo. Útil para dividir una cuenta o aplicar un porcentaje sobre la marcha.
   - **Fecha** — por defecto hoy
   - **Categoría** — requerida para Gasto y Crédito. El menú desplegable muestra el saldo **Disponible** de cada categoría junto a su nombre, así puedes elegir una con espacio sin salir del formulario.
   - **Beneficiario** — opcional, pero útil para análisis de gasto
   - **Memo** — notas opcionales
   - **Compensada** — actívalo si ya está confirmada en tu extracto
3. Haz clic en **Guardar** para cerrar el diálogo, o en **Guardar y nuevo** para mantenerlo abierto y empezar la siguiente entrada. El formulario conserva tu cuenta, tipo y fecha para que captures varias entradas rápido; el campo de monto recibe el foco automáticamente.

### Transferencias

Para una Transferencia, savr pide tanto la cuenta **origen** como la cuenta **destino**. Crea un par enlazado de transacciones — un débito y un crédito — que siempre se mueven juntas. Si editas una, la otra se actualiza. Si eliminas una, la otra se va también.

> **Por ejemplo:** Mueves $500 de Cuenta corriente a Ahorro. savr registra:
> - Cuenta corriente: -$500 (Transferencia a Ahorro)
> - Ahorro: +$500 (Transferencia desde Cuenta corriente)
> 
> Ambas transacciones comparten un emparejamiento interno. Tu patrimonio no cambia; el saldo de Cuenta corriente bajó, el de Ahorro subió.

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

> **Ejemplo trabajado:** Visita a Target, $87.43 total. De eso, $54 fueron comida y $33.43 artículos de hogar (productos de limpieza, foco, esa cosa para el gato). Una transacción, dos divisiones, dos categorías. savr muestra el monto correcto en cada categoría.

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
2. Elige la **cuenta origen** (de dónde sale el dinero — usualmente cuenta corriente).
3. Elige la **cuenta de préstamo** que se está pagando.
4. Ingresa los montos de **capital**, **interés** y **comisiones**.
5. Confirma la categoría de pago (por defecto, la vinculada al préstamo).
6. Guarda.

Tu saldo de cuenta corriente baja por el pago total, el saldo del préstamo baja por el capital, y los intereses más comisiones aparecen como gasto en la categoría de pago. Sin matemática mental.

> **Ejemplo trabajado:** Tu pago hipotecario de $1,247 son $983 capital + $251 intereses + $13 comisiones. Registras el pago como Pago de Deuda:
> - Cuenta corriente: -$1,247
> - Saldo de la hipoteca: -$983
> - Categoría Intereses Hipoteca, Gastado: +$264 (intereses + comisiones)
> 
> El siguiente mes el capital sube un poquito y los intereses bajan. savr captura esto fielmente sin que rehagas la matemática.

Para pagos en calendario, consulta [Pagos de deuda recurrentes](../recurring/#pagos-de-deuda-recurrentes).

---

## Estado compensada

Cada transacción tiene una bandera de **compensada**. Es una forma simple de marcar transacciones confirmadas por tu banco — útil cuando estás haciendo coincidir tus registros con un extracto.

Dos flujos comunes:

- Concilia contra un extracto una vez al mes, marcando cada línea conforme avanzas. (El flujo de [Conciliación](../reconcile/) de savr lo hace automáticamente — recomendado.)
- Deja las transacciones recientes sin compensar hasta que se publiquen del lado del banco.

La bandera de compensada es solo informativa — no cambia los cálculos de saldo.

---

## Editar y eliminar transacciones

Haz clic en cualquier transacción de la lista para abrir su diálogo de edición. Puedes cambiar cualquier campo, incluyendo convertir una transacción regular en dividida o viceversa. Haz clic en **Guardar** para aplicar.

Para eliminar una transacción, abre el diálogo de edición y haz clic en **Eliminar**. El saldo de la cuenta afectada se actualiza al instante. ¿Eliminaste la equivocada? Presiona **⌘Z** (Mac) / **Ctrl+Z** (Windows / Linux) para regresarla — consulta [Primeros pasos → Deshacer](../getting-started/#deshacer-cmdctrl--z).

> **Atención:** Las **transacciones de saldo inicial** son especiales. Se crean automáticamente con cada cuenta y no afectan los presupuestos. Puedes editar el monto si te equivocaste con tu saldo inicial, pero no puedes eliminar la entrada de saldo inicial sin eliminar la cuenta.

---

## Búsqueda y filtros

La parte superior de la página de Actividad tiene dos formas de acotar la lista:

### Cuadro de búsqueda

Escribe en el cuadro **Buscar actividad…** para hacer búsqueda parcial sobre:

- el **memo** de la transacción
- el **nombre del beneficiario**
- el **nombre de la categoría**
- los **nombres de las categorías de cualquier división** de esa transacción

La búsqueda no distingue mayúsculas y minúsculas, y empareja substrings — escribir `costco` encuentra "Costco Wholesale", y escribir `hogar` también saca una transacción dividida aunque su categoría principal no sea "Hogar".

Útil cuando recuerdas el nombre del lugar o lo que anotaste, pero no la fecha o el monto.

### Pills de filtro

Debajo del cuadro de búsqueda, cada filtro es una pill que puedes activar o desactivar. Tócala para fijarla; toca la **×** para quitarla.

| Filtro | Qué hace |
|---|---|
| **Cuenta** | Muestra las transacciones de una cuenta específica |
| **Categoría** | Muestra las transacciones de una categoría específica |
| **Beneficiario** | Muestra las transacciones de un beneficiario específico |
| **Tipo** | Restringe a Ingreso, Gasto, Transferencia o Crédito |
| **Rango de fechas** | Elige una fecha de inicio y fin |

Los filtros se combinan con lógica **Y** — todas las pills activas aplican. La búsqueda también se apila encima: un término de búsqueda más una pill de Tipo regresa solo los resultados que cumplen ambas.

> **Por ejemplo:** ¿Quieres ver todo lo que gastaste en "Costco" este año? Escribe "Costco" en el cuadro de búsqueda, fija la pill Tipo en Gasto, y el Rango de fechas a enero 1 → hoy. Ahí está tu número.

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

- Conciliar contra un extracto físico o en línea (o haz clic en **Conciliar** para el flujo guiado)
- Agregar varias transacciones para una cuenta rápidamente
- Revisar la actividad en un periodo específico sin configurar filtros de cuenta

Es la misma página de Actividad que ya conoces — solo más estrecha.
