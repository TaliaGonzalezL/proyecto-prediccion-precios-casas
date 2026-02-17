# proyecto-prediccion-precios-casas
Proyecto de Machine Learning para predecir el precio de viviendas usando Regresión Lineal y Scikit-Learn.
# Análisis de Segmentación de Clientes

## Resumen del Proyecto

Este proyecto es un análisis exploratorio de datos (EDA) realizado con Python y Pandas sobre un conjunto de datos de ventas de una inmobiliaria. El objetivo principal es predecir el precio de viviendas usando Regresión Lineal y Scikit-Learn.

---

## Problema de Negocio

La empresa necesita una forma clara y basada en datos para identificar y construir una herramienta que nos ayude a estimar el precio de una casa nueva que sale al mercado
---

## Proceso de Análisis

El análisis se realizó siguiendo estos pasos:

1.  **Carga de Datos:** Se creó un DataFrame en Pandas con datos de transacciones, incluyendo ID de cliente, producto y precio.
2.  **Agregación de Datos:** Se utilizó la función `.groupby()` para agrupar todas las transacciones por cliente.
3.  **Cálculo de Métricas:** Para cada cliente, se calcularon dos métricas clave:
    *   `Gasto_Total`: La suma total de dinero gastado.
    *   `Numero_Compras`: El conteo total de transacciones realizadas.
4.  **Creación de Segmentos:** Se utilizó la función `np.where` para crear una nueva columna `Segmento`, clasificando a los clientes como "Cliente VIP" si su gasto total superaba los $1000, y "Cliente Regular" en caso contrario.
5.  **Análisis Final:** Se utilizó `.value_counts()` para obtener el conteo final de clientes en cada segmento.

---

## Resultados y Conclusiones

El análisis reveló la siguiente distribución de clientes:

*   **Clientes VIP:** [Escribe aquí el número que obtuviste]
*   **Clientes Regulares:** [Escribe aquí el número que obtuviste]

Esta segmentación inicial proporciona una base clara para que el negocio comience a tratar a sus clientes más valiosos de manera diferenciada, potencialmente aumentando la lealtad y el valor de vida del cliente.

---

## Herramientas Utilizadas

*   **Lenguaje:** Python
*   **Librerías:** Pandas, NumPy
