
# Playground TensorFlow - Spiral

Creado por:

- **V. D. Betancourt**




## 🎢 Introducción

<details>
    <summary> Expandir </summary>

La captura de pantalla de la herramienta [Playground-TensorFlow](https://playground.tensorflow.org/) muestra una Red Neuronal que se está utilizando para clasificar datos estructurados en forma de **espiral**. 

![](https://github.com/vbleal/Playground/blob/main/PG_Spiral/TensorFlow_Spiral.png)

La información que se extrae, se detalla a continuación.

</details>

----------------



## 🧬 Datos

<details>
    <summary> Expandir </summary>

* **Tipo de dato**: Espiral, lo que sugiere que es un problema de clasificación no lineal.

* **Ratio de entrenamiento a datos de prueba**: 80%, lo que indica que el 80% de los datos se están utilizando para entrenar el modelo y el 20% para probarlo.

* **Ruido (Noise)**: 0, lo cual es ideal ya que significa que los datos son limpios y no hay variabilidad aleatoria que pueda confundir el modelo.

* **Tamaño de lote (Batch size)**: 10, esto significa que en cada paso de entrenamiento, la red actualizará los pesos después de procesar 10 ejemplos.



</details>

----------------



## 🧪 Hiperparámetros 

<details>
    <summary> Expandir </summary>

* **Época (Epochs)**: 600, lo cual significa que el modelo ha pasado por los datos de entrenamiento 600 veces durante el entrenamiento.

* **Tasa de aprendizaje (Learning rate)**: 0.1, que es relativamente alta, podría permitir una convergencia más rápida pero también podría provocar oscilaciones o incluso divergencia en la función de pérdida si es demasiado alta.

* **Función de activación**: Sigmoid, utilizada en cada neurona, transforma la entrada en un rango entre 0 y 1. No es ideal para redes profundas debido al problema de gradientes que se desvanecen, pero podría funcionar bien en problemas menos complejos o con menos capas.

* **Regularizació**n: Ninguna, lo que significa que no hay penalización para la magnitud de los pesos. Esto podría ser adecuado si no hay señales de sobreajuste.

* **Tipo de problema**: Clasificación, lo que significa que la red está tratando de categorizar los puntos de datos en una espiral.



</details>

----------------



## 🪪 Features (Características)

<details>
    <summary> Expandir </summary>

* **Cantidad**: 5 características distintas están siendo utilizadas como entrada. Esto incluye las coordenadas X1, X2, un término de interacción X1X2, y las funciones seno de ambas coordenadas sin(X1), sin(X2). Esto sugiere que se está tratando de capturar la no linealidad de la forma espiral.



</details>

----------------




## 🫣🔬 Capas Ocultas

<details>
    <summary> Expandir </summary>

* La red tiene 3 capas ocultas con 8, 7 y 1 neuronas respectivamente. La disminución del número de neuronas podría estar dirigida a condensar la información a una salida unidimensional para clasificación binaria.



</details>

----------------




## 📉 Resultados

<details>
    <summary> Expandir </summary>

* **Pérdida de prueba (Test loss)**: 0.012, lo que indica que el modelo tiene un rendimiento muy bueno en los datos de prueba.

* **Pérdida de entrenamiento (Train loss)**: 0.019, que también es baja, lo que sugiere que el modelo aprendió bien los datos de entrenamiento.



</details>

----------------




## 📜 Conclusiones

<details>
    <summary> Expandir </summary>

* El modelo parece estar funcionando excepcionalmente bien dado que tanto la pérdida de entrenamiento como la de prueba son bajas. Esto indica que el modelo es capaz de generalizar bien y no hay sobreajuste significativo. Sin embargo, hay que tener cuidado con la tasa de aprendizaje relativamente alta, ya que en algunos casos puede conducir a resultados subóptimos.

* La representación visual de la espiral en el gráfico de salida muestra una clara separación entre las clases, lo que confirma el buen rendimiento del modelo. La utilización de funciones trigonométricas como características de entrada es una decisión inteligente para un problema con estructura espiral, ya que estas pueden modelar patrones periódicos complejos.



</details>

----------------



