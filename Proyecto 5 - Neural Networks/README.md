# Proyecto 5 - Neural Networks: Traffic

Este proyecto pertenece al módulo **Neural Networks** del curso *CS50's Introduction to Artificial Intelligence with Python*.

## Descripción

El objetivo del proyecto es implementar una red neuronal capaz de identificar señales de tránsito a partir de imágenes. Para ello, se utiliza el dataset **GTSRB** (*German Traffic Sign Recognition Benchmark*), que contiene imágenes clasificadas en 43 categorías distintas de señales.

El modelo fue construido con **TensorFlow/Keras** y utiliza una red neuronal convolucional, ya que este tipo de arquitectura es adecuada para trabajar con imágenes.

## Conceptos aplicados

- Redes neuronales artificiales.
- Deep learning.
- Visión por computadora.
- Redes neuronales convolucionales.
- Capas convolucionales.
- Max pooling.
- Dropout.
- Clasificación multiclase.
- Normalización de imágenes.

## Archivos

- `traffic.py`: contiene la carga de datos, construcción del modelo, entrenamiento y evaluación.
- `requirements.txt`: contiene las dependencias necesarias.
- `.gitignore`: evita subir el dataset `gtsrb/` y modelos entrenados `.h5`, ya que pueden ser archivos pesados.

## Dataset

El dataset `gtsrb/` no se incluye en el repositorio debido a su tamaño. Para descargarlo dentro de la carpeta del proyecto, se puede usar:

```bash
wget -O gtsrb.zip https://cdn.cs50.net/ai/2023/x/projects/5/gtsrb.zip
unzip -o gtsrb.zip
rm gtsrb.zip
```

Cómo ejecutar

Primero se instalan las dependencias:
```bash
pip3 install -r requirements.txt
```
Después se ejecuta el programa:
```bash
python traffic.py gtsrb
```
Modelo implementado

El modelo utilizado es una red neuronal convolucional con capas Conv2D, MaxPooling2D, Flatten, una capa densa, Dropout y una capa final softmax con 43 salidas, una por cada categoría de señal.

Las imágenes fueron redimensionadas a 30 x 30 pixeles y normalizadas dividiendo sus valores entre 255.0, para que los pixeles quedaran en un rango de 0 a 1. Esta normalización mejoró significativamente el rendimiento del modelo.

Ejemplo de resultado

En una ejecución del proyecto se obtuvo un resultado aproximado de:
```text
accuracy: 0.9815
loss: 0.0817
```
Esto indica que el modelo logró clasificar correctamente una gran proporción de las imágenes del conjunto de prueba.
