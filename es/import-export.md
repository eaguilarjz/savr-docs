---
title: Importar y Exportar
parent: Español
nav_order: 10
---

> 🌐 Read this page in [English](../../en/import-export/)

# Importar y Exportar

Dos escenarios donde esta página importa:

- **Estás empezando savr con un año de historial** en otro lado (tu banco, una hoja de cálculo, otra app de presupuesto). Quieres traerlo.
- **Quieres una copia de tus datos.** Para respaldo, para impuestos, para una tabla dinámica en Excel, para tranquilidad mental.

savr maneja ambos con CSV — el formato confiable y universalmente soportado que abre en Excel, Numbers, Google Sheets y cien herramientas más.

---

## Importar transacciones desde CSV

El asistente de importación vive en **Detalle de Cuenta → Importar CSV**. Es un flujo de tres pasos diseñado para manejar la realidad caótica de las exportaciones bancarias.

> **Atención:** Las importaciones se hacen para una cuenta a la vez. Para traer un año de actividad de cheques, ahorros y una tarjeta de crédito, corre el asistente tres veces.

### Paso 1 — Subir y configurar

Elige la cuenta destino, sube un archivo CSV de tu computadora y configura cómo savr debe leerlo.

savr autodetecta lo que puede, pero a menudo necesitarás confirmar o ajustar:

| Configuración | Qué significa |
|---|---|
| **Columna de fecha** | Qué columna tiene la fecha de la transacción |
| **Formato de fecha** | mdy (mes-día-año), dmy, o ymd. Bancos de EE.UU. típicamente mdy; muchos bancos internacionales usan dmy. |
| **Columna de beneficiario** | Qué columna tiene el comercio o descripción |
| **Columna de memo** | Opcional — notas adicionales |
| **Columnas de monto** | Una sola columna con monto signado, o columnas separadas de **débito** y **crédito** |
| **Separador decimal** | `.` (EE.UU.) o `,` (la mayoría de Europa y América Latina) |
| **Separador de miles** | `,`, `.`, espacio, o ninguno |
| **Convención de signo** | Si los montos positivos significan dinero entrando o saliendo |

Una vista previa muestra las primeras 5 filas de tu CSV después de aplicar la configuración. Ajusta hasta que la vista previa se vea bien.

> **Pro tip:** Una vez que configuraste para un banco específico, savr lo recuerda. La próxima vez que subas un CSV con los mismos encabezados, la configuración se carga automáticamente. Ya no tendrás que reconfigurar.

### Paso 2 — Coincidir con transacciones existentes

Si ya capturaste algunas transacciones para esta cuenta (manualmente, en una importación previa, o por reglas recurrentes), savr no importará duplicados a ciegas. El emparejador compara cada fila del CSV contra tus transacciones no conciliadas y muestra qué encontró:

- **Coincidencia confirmada** — savr está seguro de que esta fila del CSV es la misma que una transacción existente. Las enlaza y no crea duplicado.
- **Sin coincidir** — ninguna transacción existente parece esta fila. savr creará una nueva.
- **Override manual** — puedes confirmar o rechazar cualquiera de las coincidencias de savr.

Este paso quita parte del miedo de "¿y si importo los mismos datos dos veces?" El emparejador es inteligente, pero tú tienes la palabra final.

### Paso 3 — Revisar e importar

Un resumen muestra:

- Cuántas transacciones nuevas se crearán
- Cuántas transacciones existentes se enlazarán (no se duplicarán)
- Total de entradas y salidas

Haz clic en **Importar** para ejecutar. savr crea las transacciones nuevas, enlaza las coincidencias y actualiza el saldo de la cuenta. Listo.

---

## Ejemplo trabajado de importación

Digamos que exportaste un año de actividad de tu banco como `chase-cheques-2024.csv`. Las primeras filas se ven así:

```
Transaction Date,Description,Amount,Type
01/02/2024,WHOLE FOODS MARKET 2374,-87.43,DEBIT
01/03/2024,DIRECT DEPOSIT ACME CORP,2400.00,CREDIT
01/05/2024,STARBUCKS #4112,-6.75,DEBIT
...
```

Inicias el asistente con **Cuenta = Chase Cheques** y subes el archivo. En el Paso 1:

- Columna de fecha: `Transaction Date`, formato `mdy`
- Columna de beneficiario: `Description`
- Columna de monto: `Amount` (una sola columna signada)
- Decimal: `.`, Miles: `,`
- Signo: positivo = entrada

La vista previa confirma que el primer sueldo aparece como +$2,400 ingreso, el cargo de Whole Foods como -$87.43 gasto. Se ve bien.

Paso 2 — savr no encuentra transacciones existentes con qué coincidir (es tu primera importación para esta cuenta). Creará todas las filas como nuevas.

Paso 3 — savr dice que creará 247 transacciones totalizando $34,820 entrada y $32,108 salida. Haces clic en Importar. Unos segundos después, tu cuenta Chase Cheques tiene un año de historial.

Querrás pasar unos minutos después de la importación:
- Categorizando las transacciones nuevas (se importaron con categoría vacía — savr no adivina)
- Limpiando nombres de beneficiarios (consulta [Beneficiarios → fusionar duplicados](../payees/#eliminar-un-beneficiario-y-fusionar-duplicados))

Ambos son más fáciles en bloque que transacción por transacción.

---

## Lo que la importación CSV no hace

Solo para fijar expectativas:

- **No auto-categoriza.** savr no adivina que "COSTCO" va en Comida — tú asignas categorías. (Es una característica, no una limitación: un auto-categorizador entusiasmado se equivocará en formas sutiles y hará que tus reportes mientan.)
- **Solo maneja CSV.** Si tu banco solo ofrece OFX o QIF, necesitarás convertirlo primero (Excel, un convertidor CSV, o una plantilla de hoja de cálculo).
- **Importa una cuenta a la vez.** Sin CSVs multi-cuenta.
- **No es "sincronización en vivo" con tu banco.** savr intencionalmente no es un screen-scraper o agregador de open-banking. Tú decides cuándo importar. Tú mantienes control sobre qué se registra.

---

## Exportar tus datos

Cada vista de lista en savr tiene una exportación CSV. Haz clic en el botón de exportar y savr descarga los datos como archivo `.csv`.

| Exportación | Qué obtienes |
|---|---|
| **Transacciones** | Fecha, Cuenta, Beneficiario, Categoría, Memo, Salida, Entrada, Conciliada — una fila por transacción (las divisiones se expanden a una fila por división) |
| **Cuentas** | Nombre, Tipo, Saldo, Bandera Cerrada |
| **Categorías** | Grupo, Categoría, Bandera Oculta |
| **Beneficiarios** | Nombre |

La exportación de transacciones es la grande. Abre limpia en cualquier app de hoja de cálculo, y es la base para cualquier análisis que la página de [Reportes](../reports/) de savr no cubra.

> **Por ejemplo:** ¿Quieres ver tu gasto por categoría desglosado trimestre por trimestre? Exporta transacciones, abre en tu hoja de cálculo favorita, tabla dinámica por categoría y trimestre, listo. La exportación es todo lo que necesitas.

### ¿Por qué CSV (y no OFX, QIF o JSON)?

Porque CSV abre en todo. El punto de una exportación es darte datos portables, durables y útiles — no presumir soporte de formatos. CSV hace el trabajo.

Si alguna vez necesitas una exportación estructurada para una herramienta específica, CSV también es lo más fácil de procesar con un script.

---

## Respaldos

La exportación de transacciones también es tu estrategia de respaldo. Una exportación mensual de todas las transacciones (y cuentas/categorías/beneficiarios si quieres tirantes y cinturón) es un registro lo suficientemente completo de tu cuenta de savr que podrías reconstruir desde ella si alguna vez lo necesitaras.

Guarda el archivo en algún lugar fuera de savr — tu drive en la nube, una carpeta encriptada, donde sea que sobreviva a la muerte de un solo dispositivo. No lo pienses como "si savr desaparece" (no vamos a ningún lado). Piénsalo como "si mi laptop muere el día antes de declarar impuestos."

---

## Consejos

- **Guarda tus mapeos de columnas la primera vez.** Una vez que savr conozca cómo está estructurado el CSV de tu banco, las importaciones futuras son casi de un clic.
- **Importa en orden cronológico.** Si tienes años de historial, importa el año más antiguo primero, luego el siguiente, luego el siguiente. El saldo inicial y los totales corrientes se alinearán correctamente.
- **Concilia después de una importación grande.** Corre una [conciliación](../reconcile/) en la cuenta después de importar. Atrapa los errores y confirma que savr coincide con la realidad.
- **No importes lo que ya está en tus reglas recurrentes.** Si ya configuraste un sueldo recurrente y lo aplicaste por los últimos seis meses, esas transacciones existen en savr. El emparejador debería atrapar los duplicados, pero vale la pena un vistazo.
- **Limpia beneficiarios y categorías *después* de la importación, no durante.** Intentar categorizar 247 transacciones en el flujo de importación es agotador. Solo impórtalas, luego ordénalo desde la página de Transacciones en algunas sesiones.
