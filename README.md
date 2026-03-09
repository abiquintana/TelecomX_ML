# 📊 Predicción de Cancelación de Clientes (Churn) - Telecom

## 📌 Descripción del Proyecto

La cancelación de clientes (churn) es uno de los principales desafíos para las empresas que ofrecen servicios por suscripción. Identificar a los clientes con mayor probabilidad de cancelar permite a las empresas implementar estrategias de retención de forma anticipada.

En este proyecto se analizan datos de clientes de una empresa de telecomunicaciones y se desarrollan modelos de **Machine Learning** para predecir la cancelación del servicio. A través de análisis exploratorio, transformación de variables y evaluación de modelos, se identifican los factores que más influyen en el churn.

---

## 🎯 Objetivos

- Analizar el comportamiento de los clientes y detectar patrones asociados a la cancelación.
- Construir modelos de Machine Learning para predecir el churn.
- Comparar el desempeño de diferentes modelos.
- Identificar las variables más importantes que influyen en la cancelación.
- Proponer estrategias de retención basadas en los resultados obtenidos.

---

## 📂 Dataset

El conjunto de datos contiene información sobre clientes de telecomunicaciones, incluyendo:

- Datos demográficos del cliente  
- Tipo de contrato  
- Servicios de internet  
- Servicios adicionales  
- Información de facturación  
- Tiempo de permanencia del cliente  
- Cargo mensual y cargo total  
- Estado de cancelación del servicio  

**Variable objetivo**

`baja_servicio`

- **0 → Cliente permanece**
- **1 → Cliente cancela**

---

## ⚙️ Flujo del Proyecto

El análisis sigue el flujo típico de un proyecto de Machine Learning:

1. Limpieza de datos  
2. Análisis exploratorio de datos (EDA)  
3. Transformación y codificación de variables  
4. División de datos (Train/Test Split)  
5. Manejo de desbalance de clases (SMOTE)  
6. Entrenamiento de modelos  
7. Evaluación de modelos  
8. Análisis de importancia de variables  
9. Propuesta de estrategias de retención  

---

## 🤖 Modelos Utilizados

Se entrenaron y evaluaron los siguientes modelos:

- Dummy Classifier (modelo base)  
- Árbol de Decisión  
- Árbol de Decisión con SMOTE  
- Regresión Logística  
- Random Forest (para análisis de importancia de variables)  

---

## 📈 Métricas de Evaluación

Los modelos fueron evaluados utilizando:

- Exactitud (Accuracy)  
- Precisión (Precision)  
- Recall  
- F1-score  
- Matriz de confusión  

Debido a que los datasets de churn suelen estar desbalanceados, se dio especial importancia al **recall de la clase churn**, ya que detectar clientes que podrían cancelar permite implementar estrategias de retención.

---

## 📊 Resultados Principales

Se evaluaron diferentes modelos de Machine Learning para predecir la cancelación de clientes.

El modelo de **Árbol de Decisión con balanceo de datos (SMOTE)** mostró el mejor desempeño en la detección de churn.

Resultados principales:

- Exactitud del modelo base (Dummy): **~73%**
- Exactitud del Árbol de Decisión: **~76%**
- Mejora en el recall de churn de **55% a aproximadamente 62%**
- Reducción de falsos negativos de **264 a 225 clientes**

Esto significa que el modelo logró detectar una mayor cantidad de clientes con riesgo de cancelar el servicio.

---

## 🔍 Factores que Influyen en la Cancelación

El análisis de importancia de variables y los coeficientes de regresión logística identificaron varios factores clave:

- **Tipo de contrato (Month-to-month)** → mayor probabilidad de cancelación  
- **Tiempo de permanencia del cliente** → a mayor permanencia, menor churn  
- **Cargo mensual y cargo total del servicio**  
- **Tipo de servicio de internet (Fiber optic)**  
- **Servicios adicionales como seguridad online, soporte técnico y respaldo online**

Los clientes que utilizan más servicios adicionales tienden a ser más fieles a la empresa.

---

## 💡 Estrategias de Retención

A partir de los resultados obtenidos se proponen algunas estrategias para reducir la cancelación de clientes:

- Incentivar **contratos de mayor duración** mediante descuentos o beneficios  
- Implementar **programas de fidelización para nuevos clientes**  
- Mejorar la **calidad del servicio de internet**  
- Promover **paquetes de servicios adicionales** que aumenten el valor percibido por el cliente  

---

## 🛠 Tecnologías Utilizadas

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Seaborn  
- Matplotlib  
- Google Colab  

---

## 📁 Estructura del Proyecto

TelecomX_ML  
│  
├── TelecomX_ML.ipynb (Notebook con el análisis completo)  
├── TelecomX-.csv (Dataset utilizado en el proyecto)  
└── README.md (Descripción del proyecto)

---

## 📌 Conclusión

Este proyecto demuestra cómo las técnicas de Machine Learning pueden utilizarse para predecir la cancelación de clientes y comprender los factores que influyen en su comportamiento.

El modelo de **Árbol de Decisión con SMOTE** permitió mejorar la detección de clientes con riesgo de cancelar el servicio, proporcionando información valiosa para implementar estrategias de retención basadas en datos.
