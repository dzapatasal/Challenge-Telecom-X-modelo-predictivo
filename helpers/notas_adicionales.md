**Celda 26**

- Dado que tu objetivo es **predecir los clientes que abandonan** (`Churn = 1`) y la proporción de esta clase es **26.5%**, tienes un desbalance moderado (la clase minoritaria es menos del 30%).

**Recomendación para el balanceo:**

- Si tienes **muchos datos**: Usa **undersampling** (submuestreo) de la clase mayoritaria (`Churn = 0`). Esto puede hacer que pierdas información, pero es rápido y simple.
- Si tienes **pocos datos** (o no quieres perder información): Usa **oversampling** (sobremuestreo), por ejemplo con **SMOTE**. Así aumentas la cantidad de ejemplos de la clase minoritaria (`Churn = 1`) sin eliminar datos reales.

**En la mayoría de los casos de churn, se prefiere oversampling (SMOTE)** porque:
- No pierdes información de la clase mayoritaria.
- Mejoras la capacidad del modelo para aprender patrones de la clase minoritaria.

**Resumen:**  
- Es recomendable usar **oversampling (SMOTE)** para balancear tu dataset y mejorar la predicción de clientes que abandonan.  
Luego, compara el desempeño con y sin balanceo para justificar tu elección.
---
**Celda 21**
- **Normalización**: 
- Escala los valores numéricos para que estén en un mismo rango (por ejemplo, entre 0 y 1). 

- **Balanceo**: 

- Ajusta la proporción de clases en el dataset (por ejemplo, usando sobremuestreo o submuestreo) para que no haya desbalance entre clases.

**¿Cuál va antes?**<br>

- Primero debes **balancear** las clases (si es necesario), y luego **normalizar** los datos.  
Esto es porque al crear nuevas muestras (sobremuestreo) o eliminar (submuestreo), necesitas que la normalización se aplique sobre el conjunto final de datos que usarás para entrenar el modelo.
---
**Celda 44**
- Deberia recien haber separado los datos para entrenamiento y prueba en el apartado de **Entrenamiento de modelos** (más adelante) pero como quiero verificar la multicolinealidad a traves de VIF primero tenia que obtener `X_train` ya que el `calculo VIF se realiza antes de aplicar técnicas de balanceo`