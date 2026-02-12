Predicción de Churn Bancario – Aprendizaje Supervisado
Descripción del proyecto

Este proyecto desarrolla un modelo de clasificación para predecir la probabilidad de abandono (churn) de clientes en una institución bancaria.

El objetivo principal es detectar clientes con mayor riesgo de salida, priorizando métricas como F1 y AUC-ROC debido al desequilibrio de clases presente en el dataset.

Este trabajo forma parte del curso de Aprendizaje Supervisado dentro del programa de formación en Machine Learning.

Objetivo de negocio

Identificar clientes con alta probabilidad de abandono para:

1.-Reducir la pérdida de clientes

2.-Diseñar estrategias de retención

3.-Optimizar decisiones comerciales basadas en riesgo

Dado que la clase minoritaria (clientes que abandonan) es la más relevante desde el punto de vista estratégico, se priorizó la optimización del F1-score.

Dataset

El dataset contiene información demográfica y financiera de clientes bancarios:

- CreditScore

- Geography

- Gender

- Age

- Tenure

- Balance

- NumOfProducts

- HasCrCard

- IsActiveMember

- EstimatedSalary

- Exited (variable objetivo)

Se identificó un desequilibrio de clases significativo entre clientes que permanecen y clientes que abandonan.

**Metodología**

-- Limpieza y preparación de datos

-- Eliminación de columnas no predictivas

-- Imputación de valores faltantes

-- One-Hot Encoding

-- Escalado de variables numéricas

-- División del dataset

-- Entrenamiento

-- Validación

-- Prueba

-- Uso de stratify para preservar proporción de clases

-- Modelos evaluados

-- Regresión Logística

-- Random Forest

Técnicas para manejo de desbalance

-- class_weight='balanced'

-- Upsampling de la clase minoritaria

-- Ajuste de hiperparámetros

-- Evaluación por F1 y AUC-ROC

-- Resultados

Mejor modelo en validación:

Random Forest con class_weight='balanced'
F1 (valid): 0.64
AUC-ROC (valid): 0.87

Resultados finales en test:

F1 (test): 0.606
AUC-ROC (test): 0.855

Los resultados muestran una buena capacidad discriminativa (AUC alto) y desempeño consistente entre validación y prueba, lo que indica estabilidad del modelo.

Conclusiones

La accuracy no es una métrica adecuada en escenarios con desbalance.

F1-score permite evaluar mejor la detección de la clase minoritaria.

El uso de class_weight='balanced' fue una corrección efectiva y más limpia que el re-muestreo.

Random Forest mostró mejor desempeño que la Regresión Logística en este caso.

Tecnologías utilizadas

1.- Python

2.- Pandas

3.- NumPy

4.- Scikit-learn

5.- Jupyter Notebook

Próximos pasos

Ajuste de umbral de decisión según costo de negocio

Validación cruzada

Evaluación de métricas de negocio (impacto financiero)

Implementación y monitoreo en producción
