# Proyecto 1 - Knowledge: Minesweeper

Este proyecto pertenece al módulo **Knowledge** del curso *CS50's Introduction to Artificial Intelligence with Python*.

## Descripción

El objetivo del proyecto es implementar una inteligencia artificial capaz de jugar **Minesweeper**. El programa utiliza una base de conocimiento para guardar información sobre las celdas del tablero y, a partir de ella, inferir qué celdas son seguras y cuáles pueden contener minas.

## Conceptos aplicados

- Agentes basados en conocimiento.
- Representación lógica del conocimiento.
- Inferencia a partir de información conocida.
- Uso de conjuntos para representar celdas del tablero.
- Actualización de una base de conocimiento.
- Toma de decisiones con información incompleta.

## Funcionamiento

La IA representa su conocimiento mediante oraciones del tipo:

```text
{A, B, C} = 1
```

Esto significa que, dentro del conjunto de celdas {A, B, C}, exactamente una contiene una mina.

A partir de estas oraciones, la IA puede hacer inferencias. Por ejemplo:

Si el conteo es 0, todas las celdas de esa oración son seguras.
Si el número de celdas es igual al conteo, todas esas celdas son minas.
Si una oración es subconjunto de otra, se puede generar una nueva oración con información adicional.
Archivos
minesweeper.py: contiene la lógica del juego y la implementación de la IA.
runner.py: ejecuta la interfaz gráfica del juego con pygame.
requirements.txt: contiene las dependencias necesarias.
assets/: contiene las fuentes e imágenes utilizadas por la interfaz.
Cómo ejecutar

Primero instala las dependencias:
```
pip install -r requirements.txt
```
Luego ejecuta el juego:
```
python runner.py
```
Si usas Python 3 explícitamente, también puedes usar:
```
python3 runner.py
```
Ejemplo de uso

Al iniciar el juego, se puede revelar una celda manualmente o presionar el botón AI Move para que la inteligencia artificial elija una jugada.

La IA primero intenta elegir una celda que sabe que es segura. Si no tiene suficiente información, selecciona una celda aleatoria que no haya sido jugada y que no sea conocida como mina.
