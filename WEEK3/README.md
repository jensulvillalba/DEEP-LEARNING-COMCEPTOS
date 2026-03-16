
# Red Neuronal con Backpropagation (Perceptrón de una Capa)

## Descripción del proyecto

Este proyecto implementa una red neuronal simple utilizando Python y NumPy en Google Colab. El objetivo es demostrar el proceso de aprendizaje de una red neuronal mediante el algoritmo de **backpropagation** y el uso de **funciones de activación**.

Durante el entrenamiento, el modelo ajusta sus **pesos y sesgos** para reducir el error en la predicción de un problema de **clasificación binaria**.

El proyecto permite observar cómo el error disminuye a lo largo de las épocas mediante una gráfica de entrenamiento.

---

## Objetivos

- Implementar el entrenamiento de una red neuronal simple.
- Aplicar el algoritmo de **backpropagation**.
- Utilizar funciones de activación para clasificación binaria.
- Analizar la reducción del error durante el entrenamiento.
- Validar el proceso de aprendizaje del modelo.

---

## Tecnologías utilizadas

- Python
- NumPy
- Matplotlib
- Google Colab

---

## Estructura del modelo

El modelo implementado corresponde a un **perceptrón de una sola capa**, compuesto por:

- **Capa de entrada**
- **Capa de salida**
- **Función de activación Sigmoide**

El modelo se entrena utilizando **gradiente descendente** para minimizar la función de pérdida.

---

## Dataset

Se utiliza un dataset simple de clasificación binaria basado en la compuerta lógica **AND**.

| Entrada 1 | Entrada 2 | Salida |
|----------|----------|-------|
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

---

## Proceso de entrenamiento

El entrenamiento del modelo incluye los siguientes pasos:

1. Inicialización aleatoria de pesos y bias.
2. Cálculo de la salida de la red neuronal (Feedforward).
3. Aplicación de la función de activación sigmoide.
4. Cálculo de la función de pérdida (Loss).
5. Aplicación del algoritmo de backpropagation.
6. Actualización de los pesos mediante gradiente descendente.
7. Registro del error en cada época.

---

## Resultados

Durante el entrenamiento, el modelo reduce progresivamente el error, lo cual demuestra que la red neuronal aprende a clasificar correctamente los datos.

La gráfica generada muestra la **disminución del error durante las épocas de entrenamiento**, evidenciando el proceso de aprendizaje del modelo.

---

## Ejecución del proyecto

1. Abrir el archivo del proyecto en **Google Colab**.
2. Ejecutar todas las celdas del notebook.
3. Observar los resultados del entrenamiento.
4. Analizar la gráfica de reducción del error.

---

## Conclusiones

La implementación de esta red neuronal simple permite comprender los fundamentos del aprendizaje automático. El uso de funciones de activación y el algoritmo de backpropagation permiten que el modelo ajuste sus parámetros para minimizar el error.

Los resultados muestran que incluso un modelo simple como el perceptrón puede aprender patrones en los datos cuando se aplica correctamente el proceso de entrenamiento.

---

## Autor

Proyecto desarrollado como práctica académica de **Redes Neuronales / Inteligencia Artificial**.
