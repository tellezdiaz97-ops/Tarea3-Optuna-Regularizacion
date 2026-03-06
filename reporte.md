# Tarea 3 – Optuna, Registro de Experimentos y Regularización

## Clasificación de dígitos MNIST

En esta tarea se implementó una red neuronal densa secuencial utilizando Keras para clasificar los dígitos del dataset MNIST.

---

# Búsqueda de arquitectura con Optuna

Se utilizó Optuna para probar distintas configuraciones de red neuronal variando:

- Número de capas
- Número de neuronas
- Función de activación
- Optimizador

Optuna ejecutó múltiples experimentos para encontrar la mejor arquitectura que maximiza la precisión del modelo.

Ejemplo de arquitectura encontrada:

- Capas densas: 2
- Neuronas: 128
- Activación: ReLU
- Optimizador: Adam

Esta arquitectura logró una buena precisión en el conjunto de prueba.

---

# Regularización

Después de encontrar la mejor arquitectura, se entrenó nuevamente el modelo aplicando distintos métodos de regularización.

## Regularización L1

La regularización L1 penaliza los pesos grandes del modelo y puede llevar a que algunos pesos se vuelvan cero. Esto ayuda a simplificar el modelo y reducir el sobreajuste.

## Regularización L2

La regularización L2 penaliza la magnitud de los pesos evitando que crezcan demasiado. Esto ayuda a mejorar la generalización del modelo.

## Regularización L1-L2

Combina las ventajas de L1 y L2 permitiendo controlar mejor la complejidad del modelo.

## Dropout

El método Dropout desactiva aleatoriamente neuronas durante el entrenamiento. Esto evita que el modelo dependa demasiado de ciertas neuronas y ayuda a prevenir el sobreajuste.

## Dropout + L1-L2

La combinación de Dropout con regularización L1-L2 proporciona una mayor capacidad de regularización y mejora la generalización del modelo.

---

# Conclusión

Los métodos de regularización ayudan a mejorar la capacidad de generalización del modelo y a reducir el sobreajuste. En general, Dropout combinado con regularización L1-L2 proporciona mejores resultados al entrenar redes neuronales densas.
