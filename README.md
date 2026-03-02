# proyecto-telecomX-parte2
# 📊 Predicción de Cancelación de Clientes (Churn) — Proyecto de Machine Learning

## 📌 Descripción del Proyecto

Este proyecto tiene como objetivo desarrollar un sistema de Machine Learning capaz de predecir la cancelación de clientes (Churn) en una empresa de telecomunicaciones - telecomX, identificar los factores que más influyen en la cancelación y proponer estrategias de retención basadas en los resultados.

La cancelación de clientes representa una pérdida significativa de ingresos, por lo que anticiparla permite a las empresas implementar acciones preventivas y mejorar la fidelización.

---

## 🎯 Objetivos

### Objetivo General

Desarrollar y evaluar modelos de Machine Learning para predecir la cancelación de clientes.

### Objetivos Específicos

* Limpiar y preparar el dataset
* Analizar el desbalance de clases
* Aplicar técnicas de balanceo (SMOTE)
* Entrenar múltiples modelos de Machine Learning
* Optimizar los modelos usando validación cruzada
* Evaluar el rendimiento con métricas profesionales
* Identificar las variables más influyentes en la cancelación
* Proponer estrategias de retención basadas en datos

---

## 📂 Dataset

El dataset contiene información de **7043 clientes**, incluyendo:

* Información demográfica
* Tipo de contrato
* Servicios contratados
* Cargos mensuales
* Cargos totales
* Antigüedad del cliente
* Estado de cancelación (Churn)

Variable objetivo:

```
churn
0 = Cliente activo
1 = Cliente canceló
```

---

## 🛠 Tecnologías Utilizadas

* Python 3
* Pandas
* NumPy
* Scikit-learn
* XGBoost
* Matplotlib
* Seaborn
* SMOTE (Imbalanced-learn)

---

## ⚙️ Metodología

El proyecto siguió un pipeline profesional de Machine Learning:

### 1. Carga de datos

* Lectura del archivo CSV
* Exploración inicial

### 2. Limpieza de datos

* Eliminación de columnas irrelevantes
* Verificación de valores nulos

### 3. Codificación de variables categóricas

* One-Hot Encoding

### 4. Análisis de desbalance de clases

Distribución original:

* Clientes activos: 73.46%
* Clientes cancelados: 26.54%

### 5. Balanceo de datos

Se utilizó:

```
SMOTE (Synthetic Minority Oversampling Technique)
```

Para equilibrar las clases.

---

### 6. División de datos

División estratificada:

* Entrenamiento: 80%
* Prueba: 20%

---

### 7. Normalización

Aplicada para modelos sensibles a la escala:

* Logistic Regression
* SVM
* KNN

No necesaria para:

* Random Forest
* XGBoost

---

### 8. Entrenamiento de modelos

Se entrenaron los siguientes modelos:

* Logistic Regression
* Random Forest
* XGBoost

---

### 9. Optimización de modelos

Se utilizó:

```
RandomizedSearchCV
```

Con validación cruzada de 5 folds.

---

## 📈 Resultados

| Modelo              | Accuracy | Precision | Recall | F1-score | ROC-AUC |
| ------------------- | -------- | --------- | ------ | -------- | ------- |
| Logistic Regression | 0.770    | 0.557     | 0.655  | 0.602    | 0.830   |
| Random Forest       | 0.770    | 0.563     | 0.596  | 0.579    | 0.815   |
| XGBoost             | 0.763    | 0.553     | 0.553  | 0.553    | 0.818   |

---

## 🏆 Mejor Modelo: Logistic Regression

ROC-AUC: **0.830**

Capacidad de predicción: **Alta**

El modelo puede distinguir correctamente el 83% de los casos entre clientes que cancelan y los que permanecen.

---

## 🔍 Variables más importantes

Las variables más influyentes fueron:

* Tipo de contrato (Month-to-month)
* Antigüedad del cliente (tenure)
* Cargos mensuales (monthly_charges)
* Cargos totales (total_charges)
* Tipo de servicio de internet

---

## 📊 Interpretación

Factores que aumentan la cancelación:

* Contratos mensuales
* Baja antigüedad
* Altos cargos mensuales

Factores que reducen la cancelación:

* Contratos a largo plazo
* Mayor antigüedad del cliente
* Mayor inversión acumulada

---

## 💼 Impacto Empresarial

El modelo permite:

* Identificar clientes en riesgo
* Implementar estrategias de retención
* Reducir pérdidas económicas
* Mejorar la fidelización

---

## 🧠 Estrategias de Retención Recomendadas

### 1. Incentivar contratos a largo plazo

Ofrecer descuentos por contratos de 1 o 2 años.

### 2. Programas de retención temprana

Enfocados en clientes nuevos.

### 3. Optimización de precios

Ofrecer planes más competitivos.

### 4. Intervención preventiva

Contactar clientes con alta probabilidad de cancelación.

---

## 📁 Estructura del Proyecto

```
churn-prediction/
│
├── data/
│   └── telecomX_ready_for_analysis.csv
│
├── notebooks/
│   └── churn_analysis.ipynb
│
├── models/
│   └── trained_models.pkl
│
├── README.md
│
└── requirements.txt
```

---

## ▶️ Cómo ejecutar el proyecto

### 1. Clonar repositorio

```
git clone https://github.com/LejImkoaj/proyecto-telecomX-parte2.git
```

### 2. Instalar dependencias

```
pip install -r requirements.txt
```

### 3. Ejecutar notebook

```
jupyter notebook
```

---

## 📊 Pipeline del Modelo

```
Carga de datos
   ↓
Limpieza
   ↓
Encoding
   ↓
Balanceo (SMOTE)
   ↓
Split Train/Test
   ↓
Normalización
   ↓
Entrenamiento
   ↓
Optimización
   ↓
Evaluación
   ↓
Interpretación
```

---

## 🚀 Mejoras futuras

* Deployment del modelo
* API para predicción en tiempo real
* Dashboard interactivo
* Uso de redes neuronales
* Monitoreo del modelo en producción

---

## 🎓 Nivel del Proyecto

Nivel: **Intermedio – Profesional**

Incluye:

* Pipeline completo de Machine Learning
* Optimización de modelos
* Evaluación profesional
* Interpretación de resultados
* Aplicación empresarial

---

## 👤 Autor

Proyecto desarrollado como parte de formación en Ciencia de Datos. Alura-LATAM / Oracle

---

## ⭐ Conclusión

Se desarrolló exitosamente un modelo capaz de predecir la cancelación de clientes con alta precisión, permitiendo a la empresa tomar decisiones estratégicas basadas en datos y reducir la pérdida de clientes.

---
