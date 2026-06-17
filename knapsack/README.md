# Knapsack 0/1 (Problema de la Mochila)

## Descripción del problema

El problema de la mochila 0/1 consiste en seleccionar un subconjunto de ítems, cada uno con un peso y un beneficio asociados, de manera que se maximice el beneficio total sin exceder la capacidad de la mochila. Cada ítem puede ser incluido o excluido de la solución; no se permiten fracciones de ítems.

## Instancia utilizada

Se utiliza una instancia de tipo *uncorrelated* (pesos y beneficios generados sin correlación entre sí), siguiendo la metodología propuesta en el benchmark de Pisinger, con 50 ítems.

Los datos fueron obtenidos de [David Pisinger's Optimization Codes](https://hjemmesider.diku.dk/~pisinger/codes.html). En particular, se emplean las instancias de coeficientes pequeños (*small coefficients*).

## Contenido de la carpeta

* Notebook con la  implementación y resolución en Gurobi.
* Archivo de datos correspondiente a la instancia utilizada.
* Carpeta con las instancias de prueba de coeficientes pequeños.

## Descripción de los tests

Las instancias incluidas corresponden a las presentadas por D. Pisinger en:

> Pisinger, D. (2005). *Where Are the Hard Knapsack Problems?* Computers & Operations Research.

Cada instancia tiene un nombre con el siguiente formato:

```text
knapPI_t_n_R.csv
```

donde:

* `n` es el número de ítems.
* `R` es el rango de los coeficientes.
* `t` indica el tipo de instancia:

```text
1  = uncorrelated
2  = weakly correlated
3  = strongly correlated
4  = inverse strongly correlated
5  = almost strongly correlated
6  = subset sum
9  = similar weights

11 = uncorrelated span(2,10)
12 = weakly correlated span(2,10)
13 = strongly correlated span(2,10)
14 = mstr(3R/10, 2R/10, 6)
15 = pceil(3)
16 = circle(2/3)
```

Cada archivo contiene 100 instancias diferentes.

El formato de cada instancia es:

```text
instance name
n
c
z
time
1 p[1] w[1] x[1]
2 p[2] w[2] x[2]
...
n p[n] w[n] x[n]
```

donde:

* `n`: número de ítems.
* `c`: capacidad de la mochila.
* `z`: valor óptimo de la solución.
* `time`: tiempo requerido para obtener la solución óptima.
* `p[i]`: beneficio del ítem `i`.
* `w[i]`: peso del ítem `i`.
* `x[i]`: valor de la variable de decisión en la solución óptima (`0` o `1`).
