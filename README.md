# Código de integración paralela utilizando MPI

Este repositorio contiene un código en C para realizar la integración paralela de una función utilizando la biblioteca MPI (Message Passing Interface). El código divide el intervalo de integración en segmentos y distribuye el cálculo de forma paralela entre los procesos. Al final, se realiza la suma de los resultados obtenidos en cada proceso para obtener el resultado final de la integral.

## Requisitos

- Compilador de C compatible con MPI
- Biblioteca MPI instalada

## Uso

El programa se puede ejecutar utilizando el siguiente comando:

```
mpiexec -n <num_procesos> ./integration [a] [b] [range] [n]
```

Donde:
- `<num_procesos>` es el número de procesos MPI que se utilizarán para realizar la integración.
- `a` y `b` son los límites inferior y superior del intervalo de integración, respectivamente.
- `range` es el número de segmentos en los que se divide el intervalo de integración.
- `n` es el número de particiones de cada segmento.

El programa calculará la integral de la función definida en la función `f(x)` en el intervalo `[a, b]` utilizando la fórmula de integración de Riemann. El resultado de la integral se imprimirá en la salida estándar.

## Ejemplo

A continuación se muestra un ejemplo de cómo ejecutar el programa:

```
$ make && mpiexec -l -n 8 ./barber 0 1 10 1000```

<img src="/result.png" alt="Input image" width="200" height="200"/>

## Credits

This program was created by [mirluvams](https://github.com/mirluvams) ([mirluvams@gmail.com](mailto:mirluvams@gmail.com)) and [Dr. Victor de la Luz](https://github.com/itztli) for the High Performance Computing Course 2023-2, taught by [Dr. Victor de la Luz](https://github.com/itztli) at [*Escuela Nacional de Estudios Superiores*, campus Morelia](https://www.enesmorelia.unam.mx/), [UNAM](https://www.unam.mx/).
