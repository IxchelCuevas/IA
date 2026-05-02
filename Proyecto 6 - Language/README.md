# Proyecto 6 - Language: Parser

Este proyecto pertenece al módulo **Language** del curso *CS50's Introduction to Artificial Intelligence with Python*.

## Descripción

El objetivo del proyecto es implementar un parser capaz de analizar oraciones en inglés y extraer frases nominales. Para ello, se utiliza una gramática libre de contexto, con reglas que permiten representar la estructura sintáctica de una oración.

El programa recibe una oración, la procesa, genera uno o más árboles sintácticos posibles y después identifica los **noun phrase chunks**, es decir, frases nominales que no contienen otras frases nominales dentro de ellas.

## Conceptos aplicados

- Procesamiento de lenguaje natural.
- Sintaxis y estructura de oraciones.
- Gramáticas libres de contexto.
- Símbolos terminales y no terminales.
- Árboles sintácticos.
- Tokenización.
- Extracción de frases nominales.
- Uso de NLTK.

## Archivos

- `parser.py`: contiene la gramática, el preprocesamiento de oraciones y la extracción de frases nominales.
- `requirements.txt`: contiene las dependencias necesarias.
- `sentences/`: contiene oraciones de prueba para verificar el funcionamiento del parser.

## Funcionamiento

El programa convierte la oración a minúsculas, separa el texto en palabras usando `nltk.word_tokenize` y elimina tokens que no contienen caracteres alfabéticos.

Después, usa una gramática libre de contexto para intentar construir árboles sintácticos válidos. Finalmente, busca dentro del árbol las frases nominales más pequeñas posibles, es decir, aquellas que tienen etiqueta `NP` y no contienen otra `NP` en su interior.

## Cómo ejecutar

Primero se instalan las dependencias:

```bash
pip3 install -r requirements.txt
```

Si NLTK marca error por falta de recursos de tokenización, se pueden descargar con:

```bash
python -c "import nltk; nltk.download('punkt_tab')"
python -c "import nltk; nltk.download('punkt')"
```

Para ejecutar el programa manualmente:

```bash
python parser.py
```

Ejemplo de entrada:

```bash
Holmes sat.
```

También se puede ejecutar con un archivo de prueba:

```bash
python parser.py sentences/1.txt
```

Ejemplo de salida
```
Sentence: Holmes sat.

      S
  ____|___
 NP       VP
 |        |
 N        V
 |        |
holmes   sat

Noun Phrase Chunks
holmes
```
