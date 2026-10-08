2 Ejemplos machine learning
### Ejemplo 1: Detección de correos de Spam

- **T:** Clasificar un correo electrónico entrante como "Spam" o "No Spam" (Deseado).
- **P:** Porcentaje de correos clasificados correctamente sobre el total recibido (Precisión).
- **E:** Un conjunto de miles de correos previos ya marcados explícitamente por usuarios como "Spam" o "Deseado", junto con su texto y remitente.
### Ejemplo 2: Diagnóstico médico por imágenes

- **T:** Detectar si una radiografía de tórax muestra presencia de neumonía o no.
- **P:** Porcentaje de diagnósticos correctos verificados en comparación con las evaluaciones de médicos especialistas (Sensibilidad y Especificidad).
- **E:** Base de datos de radiografías previas etiquetadas por radiólogos indicando si tenían o no neumonía.

Actividad 2.3
Glosario (Todo con base en Machine Learning)
-Pandas: Libreria de python orientada al analisis y manipulación de datos. Utiliza estructuras como los DataFrames (similares a tablas) para limpiar, filtrar y transformar conjuntos de datos.
-Matplotlib: Libreria estandar de python para la creación de gráficos e imagenes estadísticas de dos dimensiones (como histogramas, diagramas de dispersion, gráficos de lineas)
-Scikit-learn: Una de las librerias mas importantes de python para machine Learning. incluye algoritmos para clasificación, regresión agrupación(clustering), asi como herramientas para preprocesamiento y evaluación de modelos.
(iris, boston,wine, digits)a los que se pueden acceder mediante sklearn.datasets.
-Google colab: Entorno de cuadernos de jupyter ejecutable en la nube por parte de google. Permite escribir y ejecutar código Python en el navegador web con acceso gratuito a recursos como GPUs/TPUs.

Conceptos de modelado y evaluación 
Arbol de decision: algoritmo de aprendizaje supervisado que organiza las decisiones en una estructura en forma de árbol. evalua condiciones sucesivas en los atributos de los datos para llegar a una predicción final.
Matriz de confusion: Tabla utilizada en problemas de clasificación para medir el rendimiento de un modelo. compara los valores  reales contra las predicciones hechas por el modelo para identificar aciertos y errores.

sobreajuste(overfitting): Problema que ocurre cuando un modelo de machine learning memoriza en exceso lo datos de entrenamiento (incluyento el ruido o detalles insignificantes). como consecuencia, obtiene un excelente desempeño en los datos de entrenamiento pero falla al integrar generalizar sobre datos nuevos.

-Falso Positivo: Ocurre cuando un sistema, prueba o evaluación indica que algo si esta presente o ha sucedido, cuando en realidad no es asi 
-Falso Negativo: Ocurre cuando un sistema indica que algo no esta presente o ha sucedido, cuando en realidad si esta presente

Actividad 2.4

|                               | Definición                                                                                                                                             | Como Funciona                                                                                                                                                                      | Un caso de uso                                                                                       | Referencias                                                                                                                     |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| Arbol de decisión             | Modelo predictivo no paramétrico que representa un conjunto de reglas de decisión en forma de estructura de árbol.                                     | Divide los datos recursivamente en subconjuntos basados en la característica que proporcione el mayor rendimiento (usando métricas como entropía, ganancia de información o Gini). | Diagnóstico médico (clasificar si un paciente tiene o no una enfermedad en función de sus síntomas). | Quinlan, J. R. (1986). _Induction of decision trees_. Machine Learning, 1(1), 81-106.                                           |
| Regresión logistica           | Algoritmo de clasificación estadística que modela la probabilidad de que una instancia pertenezca a una categoría discreta o binaria.                  | Aplica la función sigmoide a una combinación lineal de las características de entrada para transformar las salidas en valores de probabilidad entre 0 y 1.                         | Detección de fraude financiero o clasificación de correos como spam / no spam.                       | Hosmer, D. W., Lemeshow, S., & Sturdivant, R. X. (2013). _Applied Logistic Regression_. John Wiley & Sons.                      |
| K vecinos mas cercanos (k-NN) | Algoritmo no paramétrico basado en instancias que clasifica o predice según la proximidad de los datos.                                                | Calcula la distancia (e.g., euclidiana) entre una nueva instancia y las existentes, asignando la clase más común entre sus kvecinos más cercanos.                                  | Sistemas de recomendación sencillos y reconocimiento de patrones.                                    | Cover, T., & Hart, P. (1967). _Nearest neighbor pattern classification_. IEEE Transactions on Information Theory, 13(1), 21-27. |
| Naive Bayes                   | Clasificador probabilístico basado en el teorema de Bayes con la suposición de independencia entre las variables de entrada.                           | Calcula las probabilidades a posteriori de cada clase para un conjunto de características y asigna la clase con mayor probabilidad.                                                | Clasificación de texto y análisis de sentimientos en redes sociales.                                 | McCallum, A., & Nigam, K. (1998). _A comparison of event models for Naive Bayes text classification_. AAAI Workshop.            |
| SVM                           | Algoritmo de aprendizaje supervisado utilizado para clasificación y regresión mediante la búsqueda del hiperplano óptimo.                              | Encuentra el hiperplano que maximiza el margen o distancia entre las clases de datos más cercanas (vectores de soporte).                                                           | Reconocimiento de caracteres manuscritos y clasificación de imágenes.                                | Cortes, C., & Vapnik, V. (1995). _Support-vector networks_. Machine Learning, 20(3), 273-297.                                   |
| Bosque aleatorio              | Método de ensamblado (_ensemble learning_) que combina múltiples árboles de decisión independientes para mejorar la precisión y evitar el sobreajuste. | Entrena múltiples árboles con subconjuntos aleatorios de datos y características (bagging), promediando sus predicciones o por votación mayoritaria.                               | Predicción de riesgo crediticio en banca.                                                            | Breiman, L. (2001). _Random forests_. Machine Learning, 45(1), 5-32.                                                            |
| Red Nuronal                   | Modelo computacional inspirado en la estructura biológica del cerebro humano, compuesto por capas de nodos (neuronas artificiales) interconectadas.    | Ajusta los pesos de las conexiones entre capas mediante la propagación hacia adelante y el algoritmo de retropropagación (_backpropagation_) para minimizar el error.              | Visión por computadora, procesamiento de lenguaje natural y conducción autónoma.                     | Goodfellow, I., Bengio, Y., & Courville, A. (2016). _Deep Learning_. MIT Press.                                                 |


![[Pasted image 20260930164430.png]]
¿qué pesa más: un punto más de exactitud o poder explicarle al médico por qué el sistema dijo "maligno"?

Falsos negativos. Fíjate en la columna falsos_negativos. ¿El modelo con mayor exactitud es también el que deja pasar menos tumores malignos?