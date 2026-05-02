# Proyecto 4 - Learning: Shopping

Este proyecto pertenece al módulo **Learning** del curso *CS50's Introduction to Artificial Intelligence with Python*.

## Descripción

El objetivo del proyecto es implementar un modelo de aprendizaje automático capaz de predecir si un usuario realizará una compra durante una sesión en una tienda en línea.

Para ello, se utiliza un conjunto de datos de aproximadamente 12,000 sesiones de usuarios. Cada fila representa una sesión y contiene información como páginas visitadas, duración de navegación, tipo de visitante, navegador, región, tráfico, si fue fin de semana y si finalmente hubo compra.

## Conceptos aplicados

- Aprendizaje supervisado.
- Clasificación.
- K-nearest neighbors.
- Conjunto de entrenamiento y prueba.
- Sensibilidad.
- Especificidad.
- Evaluación de modelos.

## Archivos

- `shopping.py`: contiene la implementación principal del clasificador.
- `shopping.csv`: contiene los datos utilizados para entrenar y probar el modelo.

## Funcionamiento

El programa carga los datos desde `shopping.csv` y convierte las variables categóricas a valores numéricos. Después separa los datos en conjunto de entrenamiento y conjunto de prueba.

Con el conjunto de entrenamiento se entrena un modelo **K-nearest neighbors** con `k = 1`. Luego, el modelo predice si los usuarios del conjunto de prueba realizaron una compra o no.

Finalmente, el programa evalúa el desempeño usando dos métricas:

- **Sensibilidad:** proporción de usuarios que sí compraron y fueron correctamente identificados.
- **Especificidad:** proporción de usuarios que no compraron y fueron correctamente identificados.

## Cómo ejecutar

Desde la carpeta del proyecto:

```bash
python shopping.py shopping.csv
```
Ejemplo de salida

Una ejecución del programa produjo resultados similares a los siguientes:

```
Correct: 4085
Incorrect: 847
True Positive Rate: 41.04%
True Negative Rate: 90.30%
```
Los valores pueden cambiar ligeramente en cada ejecución porque los datos se dividen aleatoriamente en entrenamiento y prueba.

Dependencias

Este proyecto requiere scikit-learn.

Para instalarlo:

```bash
pip install scikit-learn
```
