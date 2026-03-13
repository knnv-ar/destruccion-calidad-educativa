# Calculadora de poder adquisitivo docentes y nodocentes universitarios

---

## ¿Qué hace?

La calculadora realiza dos operaciones a partir de los datos que ingresa el usuario:

1. **Sueldo de referencia actualizado:** dado el sueldo neto de noviembre de 2023, calcula cuánto debería haberse cobrado en febrero de 2026 para haber empatado la inflación acumulada del período (280,32% según IPC INDEC).

2. **Pérdida real de poder adquisitivo:** si el usuario ingresa además su sueldo neto de febrero de 2026, calcula el porcentaje de poder adquisitivo perdido (o ganado) respecto de la inflación acumulada.

Todos los cálculos se ejecutan automáticamente al escribir, sin necesidad de enviar formularios ni recargar la página.

---

## Características técnicas

- **Un solo archivo HTML autocontenido** — no requiere servidor, frameworks ni dependencias externas. Se puede abrir directamente en cualquier navegador o alojar en cualquier servidor estático.
- **Formateo de números en formato argentino** — los campos de ingreso muestran automáticamente los puntos separadores de miles y la coma decimal según la convención local (ej: `1.250.000,50`). Se acepta tanto punto como coma para los centavos.
- **Responsive** — el diseño se adapta a pantallas móviles y de escritorio.
- **Sin dependencias de JavaScript externas** — toda la lógica está escrita en JS vanilla.

---

## Uso

Simplemente abrir `index.html` en cualquier navegador moderno. No se requiere instalación, servidor local ni conexión a internet.

---

## Constante de inflación

El multiplicador utilizado para los cálculos es:

```
MULTIPLICADOR_INFLACION = 3.803215
```

Corresponde a una inflación acumulada del **280,32%** entre noviembre de 2023 y febrero de 2026, según datos del Índice de Precios al Consumidor (IPC) publicados por el INDEC.

Para actualizar el cálculo a otro período, basta con modificar esta constante en el bloque `<script>` del archivo HTML, y actualizar los textos descriptivos correspondientes.
