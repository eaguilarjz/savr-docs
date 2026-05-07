---
title: Beneficiarios
parent: Español
nav_order: 7
---

> 🌐 Read this page in [English](../../en/payees/)

# Beneficiarios

Los beneficiarios son las personas, negocios o servicios al otro lado de una transacción. El supermercado. Tu casero. Ese servicio de suscripción. Tu empleador (sí — tu empleador también es un "beneficiario" en tus sueldos entrantes).

Los beneficiarios son opcionales en savr. Puedes llevar un buen presupuesto sin usarlos nunca. Pero hacen un par de cosas más fáciles — y una vez que empiezas a usarlos, te preguntas por qué no lo hacías antes.

---

## Cuándo los beneficiarios sí valen la pena

Los beneficiarios son más útiles para:

- **Preguntas sobre patrones de gasto.** "¿Cuánto gasté realmente en este restaurante el año pasado?" Un filtro, respuesta inmediata.
- **Filtrar en la página de Transacciones.** Sigue toda la actividad con una parte específica.
- **Encontrar duplicados.** Cuando ves "Costco" con 47 transacciones y "COSTCO MEXICO 234" con 3, son el mismo lugar — fusiónalos.

Si ninguno de los dos te llama la atención, sáltate los beneficiarios. savr no te va a regañar.

---

## Crear un beneficiario

De dos formas:

### En línea, mientras creas una transacción

En el campo **Beneficiario** del diálogo de transacción, simplemente escribe un nombre. Si no existe, savr lo crea automáticamente al guardar la transacción. Así es como la mayoría de la gente construye su lista de beneficiarios — naturalmente, conforme registra actividad.

### Desde la página de Beneficiarios

1. Abre **Beneficiarios**.
2. Usa el formulario **Nuevo beneficiario** en la parte superior.
3. Escribe un nombre y guarda.

Los nombres distinguen mayúsculas y minúsculas pero por lo demás son libres. Apunta a la forma que reconocerías de un vistazo: "Costco", "Spotify", "Acme Corp Nómina", no "WHL FDS MKT 2374 NW PORTLAND OR" (te vimos, exportación bancaria).

---

## Editar un beneficiario

Haz clic en cualquier nombre de beneficiario en la lista para editarlo en línea. Presiona Enter para guardar. El cambio aplica en todos lados donde se referencia el beneficiario — transacciones, reglas recurrentes, filtros.

Así es como limpias las exportaciones bancarias que destrozaron el nombre. Edita "WHL FDS MKT 2374" → "Whole Foods" y todas las transacciones relacionadas se actualizan.

---

## Eliminar un beneficiario (y fusionar duplicados)

Haz clic en la acción de eliminar en la fila del beneficiario.

- **Si el beneficiario no tiene transacciones**, se elimina al instante.
- **Si el beneficiario tiene transacciones**, savr abre un modal de **reasignación**:
  1. Elige otro beneficiario que se quede con sus transacciones (o elige **Ninguno** para dejar el campo vacío).
  2. Confirma.

En ambos casos, no se pierde ninguna transacción — solo se relinquean. Luego se elimina el beneficiario original.

> **Fusionando duplicados:** ¿Quieres fusionar "Whole Foods Market" en "Whole Foods"? Elimina "Whole Foods Market" y reasigna sus transacciones a "Whole Foods". Ambas listas se actualizan. Las transacciones se quedan donde estaban (en sus categorías correctas, con sus montos correctos) pero ahora todas están bajo un beneficiario canónico.

> **Ejemplo trabajado:** Importas un año de transacciones del banco y terminas con 14 variantes de Amazon: "Amazon", "AMAZON.COM", "Amazon Prime", "Amzn Mktp", "AMAZON DIGITAL", y así. Pasa cinco minutos eliminando cada una con reasignación a un solo beneficiario canónico "Amazon". Ahora puedes ver de un vistazo que gastaste — gulp — $38,470 en Amazon el año pasado. (De nada.)

---

## Conteo de transacciones

Cada beneficiario en la lista muestra cuántas transacciones lo referencian. Úsalo para detectar:

- **Duplicados** — dos nombres casi idénticos con conteos bajos suelen ser el mismo beneficiario. Fusiónalos.
- **Únicos** — beneficiarios con una sola transacción tal vez no valga la pena conservarlos. Puedes dejarlos, ignorarlos, o limpiarlos.

---

## Consejos

- **No te obsesiones con curarlos.** Los beneficiarios son un efecto secundario de registrar transacciones. Déjalos acumularse de forma natural y limpia periódicamente. Una limpieza de 10 minutos cada trimestre es suficiente.
- **Usa un estilo consistente.** Elige una capitalización y mantenla (p. ej. siempre con mayúscula inicial). Más fácil de escanear, más fácil de evitar duplicados.
- **Los beneficiarios de ingreso también cuentan.** "Acme Corp Nómina" o "Cliente Freelance X" en transacciones de ingreso hace que la revisión de fin de año sea *mucho* más fácil cuando intentas recordar quién te pagó cuánto.
- **Las exportaciones bancarias mienten.** Los nombres de comercio del banco suelen estar abreviados, rellenados o destrozados. Después de una importación CSV, espera pasar algunos minutos limpiando nombres de beneficiarios — es normal.
