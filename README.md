# 📊 Challenge Alura - TelecomX Parte 2

## 🤖 Predicción de Churn con Machine Learning

### 📌 Descripción del proyecto
Este proyecto tiene como objetivo predecir la evasión de clientes (**Churn**) en la empresa TelecomX utilizando técnicas de **Machine Learning**.

La evasión ocurre cuando un cliente decide cancelar el servicio, lo que representa una pérdida importante para la empresa.

A partir del análisis y modelado de los datos, se busca identificar qué factores influyen más en la cancelación y construir modelos capaces de **predecir qué clientes tienen mayor probabilidad de abandonar el servicio**.

---

### 🎯 Objetivo
El objetivo del proyecto es desarrollar **modelos predictivos** que permitan identificar clientes con riesgo de cancelación y comprender los factores que influyen en el **Churn**, ayudando a la empresa a implementar **estrategias de retención basadas en datos**.

---

### 🧰 Tecnologías utilizadas
- 🐍 Python  
- 📊 Pandas  
- 🔢 NumPy  
- 🤖 Scikit-learn  
- 📈 Matplotlib  
- 📉 Seaborn  
- 💻 Google Colab  

---

### 🧹 Preparación y tratamiento de datos
Antes de entrenar los modelos se realizaron varios pasos de preparación de los datos:

- Eliminación de la columna **customerID** por no aportar valor predictivo
- Transformación de variables categóricas mediante **One-Hot Encoding**
- Conversión del dataset a variables completamente numéricas
- Análisis de correlación entre variables
- Verificación del balance de la variable **Churn**

Distribución de la variable objetivo:

- **73.4%** clientes que no cancelan el servicio  
- **26.6%** clientes que cancelan el servicio  

---

### 🤖 Modelos de Machine Learning

Se entrenaron dos modelos de clasificación para predecir **Churn**.

#### Logistic Regression

| Métrica | Valor |
|--------|------|
| Accuracy | 0.803 |
| Precision | 0.657 |
| Recall | 0.544 |
| F1-score | 0.595 |

#### Random Forest

| Métrica | Valor |
|--------|------|
| Accuracy | 0.788 |
| Precision | 0.632 |
| Recall | 0.481 |
| F1-score | 0.547 |

El modelo **Logistic Regression** obtuvo el mejor desempeño general, logrando un mejor equilibrio entre precisión y capacidad para detectar clientes que cancelan el servicio.

---

### 📊 Variables más importantes
Los modelos identificaron varios factores relacionados con la cancelación del servicio:

- `account.Contract_Month-to-month`
- `internet.InternetService_Fiber optic`
- `account.PaymentMethod_Electronic check`
- `account.Charges.Monthly`
- `account.Charges.Total`
- `customer.tenure`

Estos resultados indican que **el tipo de contrato, el costo del servicio y la antigüedad del cliente** tienen un impacto importante en la probabilidad de cancelación.

---

### 💡 Conclusiones
El análisis y los modelos predictivos permitieron identificar patrones importantes en el comportamiento de los clientes.

Se observó que los clientes con **contratos mensuales, cargos más altos y menor tiempo en la empresa** presentan una mayor probabilidad de cancelar el servicio.

---

### 📌 Recomendaciones
Basado en los resultados del análisis se pueden implementar estrategias para reducir el **Churn**:

- Incentivar **contratos de mayor duración**
- Analizar la experiencia de usuarios de **fibra óptica**
- Revisar la **estructura de precios y cargos mensuales**
- Implementar programas de **retención para clientes nuevos**
