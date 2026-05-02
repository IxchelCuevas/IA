# Proyecto 2 - Uncertainty: PageRank

Este proyecto pertenece al módulo **Uncertainty** del curso *CS50's Introduction to Artificial Intelligence with Python*.

## Descripción

El objetivo del proyecto es implementar el algoritmo **PageRank**, utilizado para asignar importancia relativa a páginas web según los enlaces que reciben de otras páginas.

El programa analiza un conjunto de archivos HTML y calcula el PageRank de cada página mediante dos métodos: muestreo e iteración.

## Conceptos aplicados

- Probabilidad.
- Cadenas de Markov.
- Modelo del navegante aleatorio.
- Factor de amortiguamiento (*damping factor*).
- Estimación por muestreo.
- Cálculo iterativo hasta convergencia.

## Archivos

- `pagerank.py`: contiene la implementación principal del algoritmo.
- `corpus0/`, `corpus1/`, `corpus2/`: contienen conjuntos de páginas HTML para probar el programa.

## Cómo ejecutar

Desde la carpeta del proyecto:

```bash
python pagerank.py corpus0
```

También se puede probar con:

```bash
python pagerank.py corpus1
python pagerank.py corpus2
```
Funcionamiento

El método de muestreo simula a un usuario que navega aleatoriamente entre páginas. En cada paso, el usuario puede seguir un enlace de la página actual o saltar a cualquier página del corpus.

El método iterativo calcula el PageRank aplicando repetidamente la fórmula hasta que los valores convergen. Ambos métodos deben producir resultados similares.
