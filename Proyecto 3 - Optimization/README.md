# Proyecto 3 - Optimization: Crossword

Este proyecto pertenece al módulo **Optimization** del curso *CS50's Introduction to Artificial Intelligence with Python*.

## Descripción

El objetivo del proyecto es implementar una inteligencia artificial capaz de generar crucigramas automáticamente. El problema se modela como un **problema de satisfacción de restricciones** (*Constraint Satisfaction Problem*, CSP), donde cada espacio del crucigrama representa una variable y cada palabra posible pertenece al dominio de esa variable.

La IA debe elegir una palabra para cada espacio del crucigrama de manera que se cumplan todas las restricciones del tablero.

## Conceptos aplicados

- Problemas de satisfacción de restricciones.
- Consistencia de nodo.
- Consistencia de arco.
- Algoritmo AC-3.
- Búsqueda con retroceso (*backtracking search*).
- Heurística de valores mínimos restantes (*MRV*).
- Heurística de grado.
- Heurística de valor menos restrictivo.

## Archivos

- `crossword.py`: contiene las clases `Variable` y `Crossword`, que representan la estructura del crucigrama y sus variables.
- `generate.py`: contiene la lógica para resolver el crucigrama usando CSP.
- `data/`: contiene las estructuras y listas de palabras utilizadas como entrada.
- `assets/`: contiene recursos necesarios para generar la imagen del crucigrama.
- `output.png`: imagen generada como ejemplo de salida del programa.

## Funcionamiento

El programa interpreta cada secuencia de casillas vacías del crucigrama como una variable. Cada variable tiene un dominio inicial formado por todas las palabras disponibles. Después, el algoritmo reduce esos dominios aplicando restricciones.

Primero se aplica **consistencia de nodo**, eliminando palabras cuya longitud no coincide con la longitud requerida por la variable. Luego se aplica **consistencia de arco** mediante AC-3, revisando que las palabras de variables que se cruzan tengan letras compatibles en sus posiciones de intersección.

Finalmente, el programa utiliza **backtracking** para encontrar una asignación completa. Durante este proceso se usan heurísticas para elegir mejor qué variable asignar primero y en qué orden probar las palabras.

## Cómo ejecutar

Desde la carpeta del proyecto:

```bash
python generate.py data/structure1.txt data/words1.txt
```

Para generar también una imagen de salida:
```bash
python generate.py data/structure1.txt data/words1.txt output.png
```
Dependencias

Para generar la imagen de salida se necesita instalar Pillow:
```bash
pip install Pillow
```
Ejemplo de salida

En este repositorio se incluye el archivo output.png, que muestra un crucigrama generado correctamente con el programa.
