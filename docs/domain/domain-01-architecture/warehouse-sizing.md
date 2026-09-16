# Warehouse Sizing

## Sizes

La progresión indicada en la guía es:

```text
XS → S → M → L → XL → 2XL → ... → 6XL
```

Cada salto de tamaño duplica la potencia/capacidad de cómputo y el consumo de créditos indicado en la guía.

Ejemplo:

```text
XS = 1 crédito/hora
S  = 2
M  = 4
L  = 8
XL = 16
```

## Billing

La guía indica:

- cobro por segundo mientras el warehouse está encendido;
- mínimo de **60 segundos** por cada encendido.

## When to Resize

Aumentar el tamaño es la estrategia de **Scale Up**.

Caso típico:

```text
Una consulta compleja tarda demasiado
o
la consulta se queda sin memoria / hace spilling
→ considerar un warehouse más grande
```

## Do Not Confuse

```text
Warehouse size → capacidad de una ejecución
Cluster count  → capacidad para concurrencia
```

## Exam Focus

- XS → 6XL.
- Cada tamaño duplica los créditos respecto al anterior.
- Mínimo de facturación indicado: 60 segundos por encendido.
- Scale Up cambia el tamaño, no el número de clusters.

## Source

Basado en `Guia_SnowPro_COF-C03_Actualizada.pdf`.
