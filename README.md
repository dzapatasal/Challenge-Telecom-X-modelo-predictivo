![Proyecto](https://img.shields.io/badge/Proyecto-Analisis%20de%20Churn-blueviolet)
![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Status](https://img.shields.io/badge/Status-Completado-brightgreen)

# Análisis Predictivo de Churn en Clientes de Telecomunicaciones

## Objetivo General

Desarrollar un análisis exploratorio y predictivo para identificar los factores que influyen en la cancelación de clientes (churn) en una empresa de telecomunicaciones, utilizando técnicas de preprocesamiento, visualización, balanceo de clases y modelos de machine learning. El objetivo es anticipar el abandono de clientes y proponer estrategias de retención basadas en los resultados.

---

## Estructura del Repositorio

```
Challenge-Telecom-X-modelo-predictivo/
│
├── data/
│   └── datos_tratados.csv
├── notebook/
│   └── churn_clientes_modelado.ipynb
├── requirements.txt
└── .gitignore

```

- **data/**: Contiene el dataset preprocesado.
- **notebook/**: Notebook principal con el análisis y modelado.
- **requirements.txt**: Dependencias del proyecto.

---

## Herramientas y Librerías Usadas

- **Python 3.10+**: Lenguaje principal de desarrollo.
- **Jupyter Notebook**: Entorno interactivo para análisis y visualización.
- **pandas**: Manipulación y análisis de datos tabulares.
- **numpy**: Operaciones numéricas y manejo de arrays.
- **matplotlib & seaborn**: Visualización de datos.
- **scikit-learn**: Modelado predictivo, métricas y preprocesamiento.
- **imbalanced-learn (SMOTE)**: Balanceo de clases para problemas desbalanceados.
- **statsmodels**: Análisis de colinealidad (VIF).

---

## Instalación de Dependencias

Se recomienda el uso de un entorno virtual. Para instalar las dependencias:

```bash
python -m venv tu-entorno-virtual
tu-entorno-virtual\Scripts\activate  # En Windows
pip install -r requirements.txt
```

---

## Análisis Realizado

El notebook sigue una secuencia lógica y reproducible:

1. **Carga y limpieza de datos**: Eliminación de columnas irrelevantes y ajuste de tipos de datos.
2. **Codificación de variables categóricas**: Aplicación de One-Hot Encoding para el modelado.
3. **Análisis de correlación**: Identificación de variables redundantes y selección de predictores relevantes.
4. **Balanceo de clases**: Uso de SMOTE para igualar la proporción de clientes que cancelan y no cancelan.
5. **Visualización exploratoria**: Boxplots, scatter plots y heatmaps para entender patrones y relaciones clave.
6. **Entrenamiento de modelos**: Árbol de decisión y K-Nearest Neighbors, con ajuste de hiperparámetros y evaluación de desempeño.
7. **Evaluación y métricas**: Matriz de confusión, precisión, recall, F1-score y análisis de resultados.
8. **Conclusiones y recomendaciones**: Propuestas de estrategias de retención basadas en los hallazgos.

---

## Resultados Obtenidos

- **Principales factores de churn**: Antigüedad baja (tenure), bajo gasto total y tipo de contrato/método de pago.
- **Modelo más efectivo**: El árbol de decisión logra un recall alto (~0.76) para la clase "abandona", siendo el más útil para identificar clientes en riesgo.
- **Interpretación**: Los clientes nuevos y de bajo gasto son los más propensos a cancelar. El modelo permite priorizar acciones preventivas para estos segmentos.

> Para un análisis completo, visualizaciones y recomendaciones detalladas, consulta el notebook [`notebook/churn_clientes_modelado.ipynb`](notebook/churn_clientes_modelado.ipynb).

---

## Licencia

Este proyecto está bajo la licencia MIT. Consulta el archivo LICENSE para más detalles.

---

## Agradecimientos

Agradezco a **Alura LATAM** por brindar una plataforma de aprendizaje de alta calidad, recursos actualizados y una comunidad activa que impulsa el desarrollo profesional en ciencia de datos y programación.
