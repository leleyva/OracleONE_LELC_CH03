Telecom X — Modelado Predictivo de Cancelación de Clientes (Churn)
Parte II: Predicción de la Cancelación

Propósito
Este módulo corresponde a la Parte II del desafío Telecom X y tiene como objetivo principal predecir la cancelación de clientes (churn) a partir de variables relevantes del histórico de clientes. A través del análisis y modelado, se busca anticipar qué usuario tiene mayor probabilidad de abandonar la empresa, permitiendo implementar estrategias de retención más efectivas.

Estructura del Proyecto
TelecomX_LATAM_LELC_03.ipynb
Cuaderno Jupyter principal con todo el flujo: preprocesamiento, EDA, modelado, evaluación e interpretación.

/data/
Carpeta con el dataset ya limpio y tratado, usualmente en formato CSV (por ejemplo, TelecomX_data_clean.csv).

/figs/
Carpeta opcional donde se guardan visualizaciones relevantes generadas durante el análisis (matrices de correlación, matrices de confusión, importancia de variables, etc.).

Proceso de Preparación de Datos
Clasificación de variables

Categóricas: género, método de pago, tipo de contrato, servicios extra, etc.

Numéricas: antigüedad del cliente (tenure), cargos mensuales (MonthlyCharges), total gastado (TotalCharges).

Normalización y codificación

Se realiza One-Hot Encoding para transformar variables categóricas en atributos numéricos binarios.

Variables numéricas se normalizan o estandarizan según el modelo (necesario para Regresión Logística, KNN, etc.).

Separación en conjuntos de entrenamiento y prueba

División estratificada (70/30 o 80/20) para garantizar que la proporción de cancelaciones se mantenga igual en ambos conjuntos.

Justificación: Permite evaluar el desempeño real de los modelos en datos nuevos y evita sobreajuste.

Decisiones de Modelización y Justificaciones
Normalización: Aplicada solo a modelos sensibles a escala, como Regresión Logística, para asegurar que ninguna variable domine el proceso de entrenamiento.

Balanceo de clases: Evaluado si existe fuerte desbalance entre cancelaciones y no cancelaciones, utilizando técnicas como SMOTE o pesos balanceados.

Selección de modelos: Se implementan modelos lineales (Regresión Logística) y no lineales (Random Forest o Árboles) para comparar interpretabilidad versus desempeño.

Evaluación robusta: Se emplean métricas como exactitud (accuracy), precisión, recall, F1-score y análisis de matriz de confusión para medir y comparar los resultados.

Ejemplos de Gráficos e Insights
El análisis exploratorio incluye:

Heatmaps de correlación para identificar relaciones entre variables numéricas y el churn.

Boxplots y violin plots para comparar la distribución de cargos y antigüedad entre churners y clientes retenidos.

Gráficos de barras para visualizar el churn por tipo de contrato, método de pago y otros atributos categóricos.

Matriz de confusión y gráficos de importancia de variables post-modelo.

Insights destacados:

Antigüedad baja, contratos mensuales y ciertos métodos de pago están directamente asociados a mayor churn.

Los modelos permitieron identificar estas variables como los mayores factores de riesgo.
