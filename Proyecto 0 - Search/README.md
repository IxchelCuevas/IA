# Proyecto 0 - Search: Degrees

Este proyecto pertenece al módulo **Search** del curso *CS50's Introduction to Artificial Intelligence with Python*.

## Descripción

El programa calcula los grados de separación entre dos actores. Para ello, representa a los actores como nodos de un grafo y a las películas como conexiones entre ellos.

## Algoritmo utilizado

Se utilizó **Breadth-First Search (BFS)**, ya que permite encontrar el camino más corto entre dos actores cuando cada conexión tiene el mismo costo.

## Archivos

- `degrees.py`: archivo principal del programa.
- `util.py`: contiene las estructuras auxiliares `Node`, `StackFrontier` y `QueueFrontier`.
- `small/`: contiene los archivos CSV de prueba.

## Cómo ejecutar

Desde la carpeta del proyecto:

```bash
python degrees.py small
```
## Después se ingresan dos nombres de actores, por ejemplo:
```bash
Name: Kevin Bacon
Name: Tom Cruise
```
Resultado esperado

El programa muestra cuántos grados de separación existen entre los actores y la película que conecta cada paso.
