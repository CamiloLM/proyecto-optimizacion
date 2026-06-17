# Set Covering (Cobertura de Conjuntos)

## Descripción del problema

El problema de cobertura de conjuntos consiste en seleccionar el menor número posible de subconjuntos de un universo de elementos, de manera que la unión de los subconjuntos seleccionados cubra a todos los elementos del universo. Es un problema clásico de optimización combinatoria con aplicaciones en localización de servicios, asignación de turnos y diseño de redes, entre otros.

## Instancia utilizada

Instancia de 50 filas (elementos a cubrir) y 200 columnas (subconjuntos disponibles).

## Desarrollo del modelo

Además del modelo base, se desarrolla una variante del problema con modificaciones adicionales, según lo solicitado en el enunciado del caso.

## Contenido de la carpeta

- Notebook con la formulación, solución en Gurobi y análisis de resultados.
- Archivo de datos de la instancia.

## Herramientas

Python, `gurobipy`, `pandas`.
