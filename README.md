# Predicción de Precios de Viviendas con Machine Learning

## Resumen del Proyecto

Este proyecto de portafolio demuestra el proceso completo de construcción de un modelo de Machine Learning para un problema de **regresión**. Utilizando el clásico dataset "Boston Housing", el objetivo es predecir el precio mediano de las viviendas (`PRICE`) basándose en diversas características socioeconómicas y estructurales.

El proyecto abarca desde el Análisis Exploratorio de Datos (EDA) para entender las relaciones entre variables, hasta el entrenamiento, comparación y evaluación de múltiples modelos. El resultado final es un pipeline de predicción robusto y una explicación de los factores más influyentes en sus decisiones.

---

## Problema de Negocio

Para agentes inmobiliarios, desarrolladores y compradores, estimar el valor de una propiedad de manera precisa es fundamental. Un modelo predictivo confiable puede automatizar y mejorar la precisión de las tasaciones, identificar propiedades infravaloradas o sobrevaloradas y ayudar a entender qué características impactan más en el valor de mercado de una vivienda.

---

## Proceso de Análisis y Modelado

El proyecto se desarrolló siguiendo un ciclo de vida estructurado de ciencia de datos:

1.  **Análisis Exploratorio de Datos (EDA):** Se investigaron las distribuciones de las variables y las relaciones entre ellas. Se utilizó un **mapa de calor de correlaciones** para identificar las características con mayor impacto en el `PRICE`. El análisis confirmó que `RM` (número de habitaciones) tiene una fuerte correlación positiva y `LSTAT` (% de estatus bajo) tiene una fuerte correlación negativa con el precio.

2.  **Preparación de Datos:** Los datos se dividieron en conjuntos de entrenamiento (80%) y prueba (20%) para asegurar una evaluación honesta del rendimiento del modelo.

3.  **Construcción de Pipelines:** Para garantizar un preprocesamiento robusto y consistente, se utilizaron `Pipelines` de Scikit-Learn. Cada pipeline incluía un paso de **escalado de características** (`StandardScaler`) para normalizar los datos antes de pasarlos al modelo.

4.  **Experimentación de Modelos:** Se entrenaron y evaluaron dos modelos diferentes para comparar su rendimiento:
    *   **Modelo Baseline:** `LinearRegression`, para establecer un punto de partida.
    *   **Modelo Avanzado:** `RandomForestRegressor`, para capturar relaciones más complejas y no lineales.

5.  **Evaluación:** El rendimiento de cada modelo se midió utilizando dos métricas clave para regresión:
    *   **Error Absoluto Medio (MAE):** Mide el error promedio de las predicciones en dólares.
    *   **Coeficiente de Determinación (R²):** Mide el porcentaje de la variabilidad en los precios que el modelo es capaz de explicar.

---

## Resultados y Conclusiones

La experimentación demostró que el modelo `RandomForestRegressor` tuvo un rendimiento significativamente superior al baseline de `LinearRegression`.

*   **Modelo Ganador:** `RandomForestRegressor`
*   **R² (Coeficiente de Determinación):** 0.89
*   **MAE (Error Absoluto Medio):** $2.07k

Un **R² de 0.89** indica que nuestro modelo es capaz de **explicar el 89%% de la variabilidad en los precios de las viviendas** utilizando las características proporcionadas. El MAE nos dice que, en promedio, las predicciones del modelo tienen un error de aproximadamente **$2,070]**.

---

## Interpretabilidad del Modelo

Para entender *por qué* el modelo toma sus decisiones, se analizó la importancia de las características (`Feature Importance`). El análisis revela que el modelo basa sus predicciones principalmente en los dos factores identificados durante el EDA, lo que confirma que está aprendiendo patrones lógicos.

<img width="882" height="548" alt="Importancia_caracteristicas" src="https://github.com/user-attachments/assets/21bafd72-82d2-444b-a57d-2a7838997ae6" />


---

## Herramientas Utilizadas

*   **Lenguaje:** Python
*   **Librerías Principales:** Pandas, NumPy, Scikit-Learn, Seaborn, Matplotlib
*   **Flujo de Trabajo:** Git, GitHub, Google Colab
