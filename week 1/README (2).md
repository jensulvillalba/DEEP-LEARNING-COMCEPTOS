


# 🧠 Redes Neuronales Básicas

## 📌 Descripción

En esta actividad se implementan modelos básicos de redes neuronales utilizando Python y NumPy, con el fin de comprender el funcionamiento de una neurona artificial y el proceso de clasificación binaria.

---

## 🎯 Conceptos trabajados

* Entradas
* Pesos
* Bias (sesgo)
* Cálculo de z = w·x + b
* Función de activación
* Salida binaria (0 o 1)

---

## 🧠 Implementación

### 🔹 Perceptrón

Se implementa un perceptrón que clasifica correctamente datos linealmente separables (compuerta AND).
Incluye entrenamiento y gráfica de error por época.

---

### 🔹 Red neuronal de una capa

Se implementa una red simple utilizando operaciones matriciales con NumPy y función de activación sigmoide.

---

### 🔹 Red neuronal multicapa

Se implementa una red con una capa oculta (ReLU) y una capa de salida (Sigmoid).
Se realiza únicamente el cálculo hacia adelante (forward).

---

## ⚙️ Uso de NumPy

Se utilizan operaciones como:

* Multiplicación matricial (`np.dot`)
* Sumas y transposiciones

---

## 📊 Resultados

* El perceptrón clasifica correctamente la compuerta AND
* El error disminuye durante el entrenamiento
* Se evidencia el uso de funciones de activación en cada modelo

---

## 📌 Conclusión

Se logró implementar y entender el funcionamiento básico de redes neuronales, desde un perceptrón hasta una red multicapa simple.
