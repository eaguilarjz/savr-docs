> 🌐 Read this page in [English](../en/getting-started.md)

# Primeros pasos con savr

savr es una aplicación de presupuesto de base cero — cada unidad de tus ingresos tiene un trabajo antes de que lo gastes. Cuando tu presupuesto está equilibrado, el monto **Por presupuestar** llega a cero y sabes exactamente a dónde va tu dinero.

## Cómo funciona savr

1. **Agrega tus cuentas** — cuenta corriente, ahorros, tarjetas de crédito, préstamos, efectivo.
2. **Crea categorías** — agrupa gastos similares (Vivienda, Comida, Transporte, etc.).
3. **Presupuesta tus ingresos** — asigna todo el dinero disponible a categorías hasta que no quede nada sin asignar.
4. **Registra tus transacciones** — cada compra reduce el saldo disponible de la categoría correspondiente.
5. **Ajusta sobre la marcha** — si te excedes en una categoría, mueve dinero de otra.

---

## Configuración rápida (primera vez)

### 1. Crea tus cuentas

Ve a **Cuentas** y agrega cada cuenta que quieras rastrear. Ingresa el saldo actual de hoy — este es tu punto de partida.

Para tarjetas de crédito, ingresa el saldo adeudado como número positivo (ej. `450.00`). Para préstamos, también ingresarás la tasa de interés y el pago mensual.

### 2. Configura las categorías

Ve a **Categorías** y organiza tus gastos en grupos y categorías. Puedes usar emojis y caracteres unicode en los nombres para hacerlos más visuales y fáciles de identificar de un vistazo:

```
🏠 Vivienda
  ├─ Renta / Hipoteca
  └─ Servicios

🍔 Comida
  ├─ Supermercado
  └─ Restaurantes

🚗 Transporte
  ├─ Gasolina
  └─ Seguro
```

Puedes arrastrar categorías y grupos para reordenarlos en cualquier momento.

### 3. Presupuesta este mes

Ve a **Presupuesto**. El banner **Por presupuestar** muestra tu dinero total sin asignar. Haz clic en el monto de **Presupuestado** junto a cualquier categoría y escribe cuánto quieres asignar. Presiona **Enter** para guardar o **Escape** para cancelar. Continúa hasta que el banner muestre **0.00** y aparezca un mensaje de felicitación.

Si tienes objetivos configurados, usa **Auto-asignar** o **Llenar por objetivos** para llenar las categorías automáticamente.

### 4. Registra tus gastos

Cada vez que gastes dinero, agrega una transacción en la página de **Transacciones** o directamente dentro de una cuenta. Selecciona la categoría correcta y el saldo disponible se actualiza al instante.

---

## Conceptos clave

### Por presupuestar (TBB)

La cantidad de ingresos que aún no has asignado a ninguna categoría. Este número debe llegar a **cero** — no debe ser negativo. Si es negativo, has presupuestado más de lo que tienes y necesitas reducir algunas categorías.

El banner muestra una frase motivacional rotatoria que cambia cada vez que el escenario cambia (dinero por asignar, totalmente presupuestado, excedido). La frase usa el nombre de tu moneda configurada automáticamente.

### Saldo disponible

Cada categoría muestra un monto **Disponible**: lo que presupuestaste más el remanente del mes anterior, menos lo que gastaste. Una **barra de progreso** debajo del nombre de la categoría muestra la proporción de gasto de un vistazo. Si el saldo disponible se vuelve rojo, te has excedido y necesitas cubrirlo moviendo dinero de otra categoría.

### El panel de detalle de categoría

Haz clic en cualquier fila de categoría para abrir un panel de detalle en el lado derecho. Muestra un desglose de remanente, dinero asignado, gastos en efectivo, gastos con tarjeta de crédito y el saldo neto disponible. También permite aplicar estrategias de auto-asignación por categoría y gestionar el objetivo de la categoría, todo sin salir de la página de presupuesto.

### Objetivos

Un objetivo es una meta para una categoría — cuánto quieres presupuestar cada mes, semana o año. Los objetivos impulsan las funciones de **Auto-asignar** y **Llenar por objetivos**.

### Remanente

Cuando una categoría tiene dinero sobrante al final del mes y el remanente está activado, ese excedente se traslada al saldo disponible del mes siguiente.
