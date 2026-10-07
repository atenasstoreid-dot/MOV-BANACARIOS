# Movimientos bancarios – reglas de registro

Este repositorio guarda solo las reglas para anotar movimientos en la hoja
"Base de datos" del archivo de movimientos bancarios (Drive). **Nunca** se
suben aquí extractos, valores, cédulas, nombres de terceros ni filas de la
base: esa información es confidencial y se trabaja solo en la sesión.

## Columnas

| Col | Contenido | Regla |
|---|---|---|
| A | ID | Consecutivo, sigue al último ID de la base |
| B | Cuenta bancaria | Nombre exacto ya usado en la base (el de más uso si hay variantes, p. ej. `T.C AMEX ` con espacio) |
| C | Fecha | Fecha del movimiento |
| D | Tipo | `INGRESO` o `EGRESO` según el signo del extracto |
| E / F | Cod UN / Unidad de negocio | Según la cuenta (histórico): #A9076, VISA 9462, NEQUI, WALLLET EFFI, EFECTIVO BODEGA/OFICINA, CDT ATENAS → `01` SAS · #8855, T.C AMEX, AMEX DOLARES, CREDITO HIP, CDT IVAN → `02` IAVS · #4023, T.C DIANA → `04` DMON |
| G | Concepto | Solo si el histórico es consistente para ese tipo de movimiento o tercero; si no, en blanco y se reporta |
| H / I | Cédula-NIT / Nombre tercero | Hojas `proveedores`, `empleado`, `NIT PDTE` e histórico; si no hay certeza, en blanco |
| J | Moneda | `COP` (USD solo en AMEX DOLARES) |
| K / M | Valor / Valor COP | Valor absoluto |
| L | ID beneficiario x dist. | Ignorar (vacía) |
| N | Concepto agrupado | Solo si el concepto G siempre va al mismo grupo en el histórico |
| O | Valor neto | Negativo si es EGRESO |

## Reglas de clasificación confirmadas por el usuario

1. **Ingresos por transferencia a BANCOLOMBIA #A9076** (transferencia de otra
   cuenta, desde Nequi o por llave) que **no** correspondan a un pago
   recurrente identificado → G = `PAGO CLIENTE`, H = `-`, I = `-`,
   N = `08 Trasferencia`.

2. **Traslados con el fondo de inversión (Fiducuenta)** desde/hacia
   #A9076 → N = `08 Trasferencia` (el usuario corrigió el 05 que se usaba antes;
   algunos egresos al fondo los reclasifica él como provisiones).
3. **Pagos de tarjeta AMEX desde #A9076** → N = `08 Trasferencia`.

### T.C VISA 9462 (según histórico y correcciones del usuario)

- `FACEBK *...` → G `GASTOS PUBLICIDAS ATENAS`, I `META `, N `06 Gasto publicidad`.
- `ABONO SUCURSAL VIRTUAL` (pago de la tarjeta, valor negativo) → `INGRESO`,
  G `PAGO TAJETA DE CREDITO VISA `, I `TRANFERENCIA DE PAGOS `, N `08 Trasferencia`.
- `OPENAI` → `OPENAI MEMBRESIA` / `12 Gastos administrativos`.
- `ANTHROPIC` → `GASTO PERSONAL ANTHROPIC` / `09 Dividendos`.
- Comercios no empresariales (restaurantes, tiendas, apps personales) →
  G `GASTO PERSONAL <COMERCIO>`, N `09 Dividendos` (marcar como sugerido).
- Otros abonos/reversos negativos → en blanco y reportar.

## Reglas generales

- **Antes de generar filas**, descargar la versión más reciente de la base:
  el ID nuevo es el máximo ID existente + 1, y hay que descartar los
  movimientos que ya estén anotados (misma cuenta, fecha, tipo y valor).
  Reportar filas de la base que no aparezcan en el extracto (posibles
  duplicados) e IDs repetidos.

- No saltarse ningún movimiento: cuadrar cantidad y totales contra el extracto.
- Lo que no se sepa con certeza se deja en blanco y se reporta con el motivo.
- Entregar las filas en una hoja nueva y privada del Drive del usuario (el
  conector de Drive no puede escribir dentro del archivo existente).
