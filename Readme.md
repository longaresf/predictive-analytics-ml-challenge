# Predictive Analytics & Advanced Machine Learning Pipeline

Este repositorio contiene la resolución de un desafío técnico especializado en **Ciencia de Datos y Aprendizaje Automático**. El proyecto destaca por la construcción de un flujo de trabajo analítico automatizado (*Machine Learning Pipeline*) que abarca desde el análisis exploratorio y preprocesamiento avanzado de datos, hasta el modelado predictivo utilizando algoritmos de última generación en la industria como **XGBoost** y **LightGBM**.

## 🚀 Capacidades Técnicas Implementadas

* **Análisis Exploratorio de Datos (EDA):** Diagnóstico estadístico univariado y multivariado de las variables del entorno, identificando correlaciones, sesgos y patrones ocultos mediante visualizaciones avanzadas con `Seaborn` y `Matplotlib`.
* **Pipelines de Preprocesamiento Automatizado:** Uso de `ColumnTransformer` y `Pipeline` para ejecutar de forma secuencial y aislada la imputación de nulos (`SimpleImputer`), codificación de variables categóricas (`OneHotEncoder`) y escalamiento numérico (`StandardScaler`).
* **Modelado Predictivo Multialgoritmo:** Entrenamiento, evaluación y comparación de múltiples arquitecturas de aprendizaje supervisado para optimizar la clasificación:
  * Modelos Lineales y Basados en Distancia: `LogisticRegression` y `KNeighborsClassifier`.
  * Modelos Basados en Árboles y Ensambles (Boosting): `DecisionTreeClassifier`, `XGBClassifier` y `LGBMClassifier`.
* **Optimización y Validación Cruzada:** Ajuste fino de hiperparámetros mediante `GridSearchCV` combinado con estrategias de validación robustas (`cross_val_score`) para garantizar la capacidad de generalización del modelo.
* **Evaluación Métrica Exhaustiva:** Diagnóstico de rendimiento mediante matrices de confusión, curvas ROC-AUC, y métricas de *Accuracy*, *Precision*, *Recall* y $F_1$-Score para un control estricto de falsos positivos y negativos.

## 🛠️ Stack Tecnológico

* **Lenguaje Core:** Python 3.x
* **Manipulación de Datos:** `Pandas`, `NumPy`
* **Visualización Gráfica:** `Seaborn`, `Matplotlib`
* **Modelado y Pipeline:** `Scikit-Learn` (Sklearn)
* **Algoritmos de Gradient Boosting:** `XGBoost`, `LightGBM`

## ⚙️ Arquitectura del Pipeline y Solución de Problemas

El desarrollo de este motor analítico se centró en resolver desafíos críticos de ingeniería de características (*Feature Engineering*):

1. **Prevención de Fuga de Datos (*Data Leakage*):** Al encapsular el preprocesamiento dentro de un `Pipeline` de Sklearn antes del entrenamiento, se garantiza que los estadísticos (como la media del escalador o las modas de la imputación) se calculen exclusivamente con el conjunto de entrenamiento (*Train Set*), protegiendo la integridad del conjunto de validación (*Test Set*).
2. **Eficiencia en Datos Estructurados:** La inclusión de **XGBoost** y **LightGBM** permite procesar relaciones no lineales complejas entre las variables con tiempos de ejecución optimizados, superando las limitaciones de los árboles de decisión tradicionales.
3. **Métricas Alineadas al Negocio:** El análisis no se limitó a evaluar la exactitud global (*Accuracy*). Se implementó el balance entre *Precision* y *Recall* mediante la métrica $F_1$-Score, asegurando que el modelo sea robusto incluso ante conjuntos de datos con desbalance de clases.

## 🔧 Configuración e Instalación Local

Para replicar los experimentos, auditar las transformaciones o ejecutar las predicciones locales utilizando entornos virtuales, sigue estos pasos:

1. **Clonar el repositorio:**
   ```bash
   git clone [https://github.com/longaresf/predictive-analytics-ml-challenge.git](https://github.com/longaresf/predictive-analytics-ml-challenge.git)
   ```
2. Ingresar al directorio de trabajo:
   Bash
   cd predictive-analytics-ml-challenge

3. Configurar y activar el entorno virtual (Ejemplo con Conda):
   Bash
   conda create --name ml-pipeline python=3.9
   conda activate ml-pipeline

4. Instalar las librerías del sistema:
   Bash
   pip install -r requirements.txt

5. Ejecutar el Jupyter Notebook:
   Bash
   jupyter notebook

   Abre el archivo principal para visualizar secuencialmente el análisis exploratorio y la ejecución de la grilla de modelos.

Autor

    Francisco Longares - Científico de Datos & Desarrollador de Soluciones IA - longaresf
