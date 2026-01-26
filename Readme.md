# Entrevista CENS — Calculadora de pérdida (%)

Pequeña página web (HTML + CSS + JavaScript) para calcular el porcentaje de pérdida con base en:

- **Entregada**: Energía total del transformador (kWh)
- **Consumida**: Suma de consumo de los clientes (kWh)

La app muestra el porcentaje calculado y un indicador visual según un umbral.

## Fórmula

\[\text{pérdida \%} = \frac{\text{consumida}}{\text{entregada}} \times 100\]

## Reglas visuales

- Si **pérdida % > 15%**: muestra **"Revisión prioritaria"** en rojo.
- Si **pérdida % ≤ 15%**: muestra **"Normal"** en verde.

> El umbral se configura en el JS con `UMBRAL_REVISION_PRIORITARIA = 15`.

## Cómo usar

1. Abre el archivo [index.html](index.html) en tu navegador (doble clic).
2. Ingresa:
   - **Energía total del transformador (kWh)** (Entregada)
   - **Suma de consumo de los clientes (kWh)** (Consumida)
3. El resultado se actualiza automáticamente mientras escribes.

## Validaciones

- Si el valor **Entregada** es `0` o menor, se muestra un mensaje indicando que debe ser mayor a 0.
- Se aceptan decimales con **coma o punto**.

## Estructura

- [index.html](index.html): UI, estilos y lógica de cálculo.

## Nota sobre el fondo

El fondo usa una imagen cargada desde el sitio de CENS mediante una URL directa. Si esa URL cambia o no carga por conexión, puedes reemplazarla en el CSS del `body`.
