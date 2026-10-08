# Predicción de Regímenes de Mercado y Retornos con Machine Learning

Este repositorio contiene el trabajo de investigación cuantitativa y aplicación de algoritmos de **Machine Learning (Random Forest Regressor & Classifier)** para la predicción de la dirección y retornos de activos financieros (NKE, BRK-B, NVDA).

El proyecto fue desarrollado como entrega final del módulo de Inteligencia Artificial aplicada al Trading Algorítmico (TradeSpark / A3 Academia).

## 🧠 Enfoque Cuantitativo y Metodología

El modelo aborda el desafío de la predictibilidad en series de tiempo financieras mediante dos enfoques:

1. **Enfoque de Regresión (Laboratorio):** Intento de predicción de retornos continuos utilizando rezagos (*Lags*) y volatilidad implícita diaria.
2. **Enfoque de Clasificación Binaria (Estratégico):** Transformación del problema a la predicción de dirección del movimiento (Alza/Baja) aplicando un **Umbral de Confianza (58%)** como filtro de ruido y optimizador de *Precision*.

## 📊 Métricas de Evaluación Implementadas

* **Métricas de Regresión:** Evaluación mediante R² Score, MAE (Mean Absolute Error) y RMSE (Root Mean Squared Error).
* **Evaluación de Dirección:** Matriz de Confusión analítica (VP, VN, FP, FN) e informe de clasificación (Precision, Recall, F1-Score).

## 📈 Conclusiones del Modelo

El análisis demuestra que en entornos de alta eficiencia de mercado, la predicción de retornos continuos tiende a sobreajustar (*overfitting*). Sin embargo, la implementación de un **clasificador con umbral de certeza** demostró efectividad para mitigar falsos positivos, optimizando la toma de decisiones en mesas de dinero al seleccionar únicamente ruedas con alta probabilidad de acierto.

## 🛠️ Tecnologías Utilizadas

* **Python 3**
* **Scikit-Learn** (RandomForestRegressor, RandomForestClassifier, TimeSeriesSplit)
* **Pandas & NumPy** (Ingeniería de Features y Lags)
* **YFinance** (Ingesta de Market Data histórica)
* **Matplotlib** (Visualización de curvas de equidad y matrices de confusión)
