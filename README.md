# Desarrollo de un Modelo Predictivo para Identificar el Riesgo de Suicidio

## Definición del Problema y Objetivos

El objetivo principal de este proyecto es desarrollar un modelo predictivo para identificar individuos con alto riesgo de suicidio utilizando el conjunto de datos "master.csv", al que llamaremos "suicide_rates_survey". Este modelo tiene la finalidad de asistir en la implementación de intervenciones preventivas efectivas, basadas en un análisis detallado de los factores demográficos asociados al riesgo de suicidio.

## Conjunto de datos

Este conjunto de datos, proporcionado por la OMS, incluye estadísticas sobre suicidios desde 1985 hasta 2016. Contiene información detallada sobre:

- Tasas de suicidio por país, edad, y género.
- Características demográficas y económicas como el PIB y el Índice de Desarrollo Humano (IDH).
- Datos de población por grupo de edad y año.

## Proceso de Ciencia de Datos

### 1. Definición de Datos a Obtener y Carga de Datos

- **Descarga**: Obtendremos el conjunto de datos "master.csv" desde Kaggle.
- **Carga en el Entorno de Análisis**: Importaremos los datos en un entorno Jupyter Notebook para su análisis.

### 2. Limpieza de Datos

- **Revisión y Manejo de Valores Nulos**: Identificaremos y trataremos los valores faltantes y cualquier dato inconsistente.
- **Normalización de Unidades y Categorías**: Ajustaremos las unidades de medida y los formatos de las categorías para asegurar la coherencia.
- **Limpieza de Duplicados y Corrección de Errores Tipográficos**: Eliminaremos duplicados y corregiremos errores en los datos.

### 3. Exploración de Datos

- **Análisis Descriptivo**: Realizaremos un análisis descriptivo para comprender la distribución de las variables en el conjunto de datos.
- **Visualizaciones**: Usaremos gráficos de barras, histogramas y mapas de calor para identificar patrones y relaciones significativas.
- **Análisis de Correlación**: Evaluaremos las correlaciones entre variables demográficas y las tasas de suicidio para detectar factores de riesgo.

### 4. Selección del Modelo

1. **Regresión Logística**
   - **LogisticRegression**: Modelo de regresión para clasificación binaria o múltiple basado en la estimación de probabilidades.
2. **Máquinas de Vectores de Soporte (SVM)**
   - **SVC**: Support Vector Classification para clasificación de datos, que busca maximizar el margen entre las clases.
   - **LinearSVC**: Versión de SVC que utiliza un clasificador lineal, más eficiente para grandes conjuntos de datos.
3. **Bosques Aleatorios**
   - **RandomForestClassifier**: Modelo de ensamblaje que combina múltiples árboles de decisión para mejorar la precisión y controlar el sobreajuste.
4. **K-Vecinos Más Cercanos (KNN)**
   - **KNeighborsClassifier**: Clasificador basado en la proximidad, que asigna una clase en función de las clases de los k vecinos más cercanos.
5. **Naive Bayes**
   - **GaussianNB**: Clasificador basado en el teorema de Bayes con la suposición de que las características siguen una distribución normal.
6. **Perceptrón**
   - **Perceptron**: Modelo de clasificación lineal que se entrena mediante un algoritmo de descenso de gradiente.
7. **Clasificador de Descenso de Gradiente Estocástico**
   - **SGDClassifier**: Clasificador que utiliza el descenso de gradiente estocástico para optimizar un modelo lineal.
8. **Árboles de Decisión**
   - **DecisionTreeClassifier**: Clasificador que usa un árbol de decisión para dividir los datos en función de características.

**Justificación**: Estos modelos son adecuados para tareas de clasificación binaria y pueden manejar tanto variables categóricas como continuas, permitiendo una evaluación robusta del riesgo de suicidio.

### 5. Entrenamiento y Evaluación del Modelo

- **División de Datos**: Separaremos los datos en conjuntos de entrenamiento, prueba y validación.
- **Entrenamiento de Modelos**: Utilizaremos validación cruzada para entrenar los modelos y evitar el sobreajuste.
- **Evaluación del Rendimiento**: Mediremos los siguientes indicadores:
  1. **Exactitud (Accuracy)**
     - `accuracy_score`: Mide la proporción de predicciones correctas sobre el total de predicciones realizadas.
  2. **Precisión (Precision)**
     - `precision_score`: Mide la proporción de verdaderos positivos sobre el total de positivos predichos.
  3. **Recuperación (Recall)**
     - `recall_score`: Mide la proporción de verdaderos positivos sobre el total de positivos reales.
  4. **Puntuación F1 (F1 Score)**
     - `f1_score`: Media armónica entre precisión y recuperación, útil para evaluar el rendimiento en casos de desequilibrio de clases.
  5. **Matriz de Confusión**
     - `confusion_matrix`: Matriz que muestra los verdaderos positivos, falsos positivos, verdaderos negativos y falsos negativos.
  6. **Informe de Clasificación**
     - `classification_report`: Informe que incluye precisión, recuperación y puntuación F1 para cada clase, además del soporte.
  7. **Curva ROC y AUC**
     - `roc_curve`: Calcula la curva de características operativas del receptor (ROC) para la evaluación de clasificación.
     - `auc`: Calcula el área bajo la curva ROC (AUC), que proporciona una medida del rendimiento general del modelo de clasificación.

### 6. Representación Final de los Resultados

- **Dashboard**: Crearemos un dashboard para visualizar las predicciones y probabilidades de riesgo de suicidio.
- **Gráficos de Importancia de Características**: Mostraremos cuáles características tienen el mayor impacto en la predicción del riesgo de suicidio.
- **Tasas de Predicción por Grupos Demográficos**: Presentaremos las tasas de predicción diferenciadas por grupos demográficos para identificar áreas de mayor riesgo.

## Conclusiones

Al finalizar el proyecto, se redactarán conclusiones basadas en los resultados obtenidos del análisis y modelado. Se evaluará la efectividad del modelo predictivo y se propondrán mejoras. Se resumirá lo aprendido a partir del análisis de datos y el proceso de modelado para ofrecer recomendaciones concretas en la prevención del suicidio.

## Limitaciones y Mejoras Futuras

El conjunto de datos actual presenta limitaciones, especialmente en términos de cobertura geográfica. Para mejorar la precisión del modelo, se recomienda la recopilación de datos adicionales como:

- Historial de intentos de suicidio.
- Información sobre suicidios en familiares cercanos.
- Presencia de enfermedades mentales en la familia.
- Uso de medicamentos para trastornos mentales.
- Participación en terapia o búsqueda de ayuda.
- Orientación sexual y cambios de género.
- Experiencias de bullying y violencia.
- Situación económica de la persona.

Estas adiciones permitirían una evaluación más completa y precisa del riesgo de suicidio, mejorando la capacidad del modelo para hacer predicciones efectivas.
