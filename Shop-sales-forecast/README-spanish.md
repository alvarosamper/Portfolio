Predicción de Ventas para Tiendas
Este proyecto busca ayudar a una tienda a predecir sus ventas futuras utilizando modelos de aprendizaje automático. Estas predicciones permiten optimizar la gestión de inventario, evitar la falta de productos en stock y, en general, mejorar la planificación estratégica.

Objetivos
Realizar un análisis exhaustivo de los datos históricos de ventas.
Desarrollar y optimizar modelos de predicción de ventas.
Desplegar un modelo final que pueda utilizarse fácilmente para generar predicciones en tiempo real.
Contenido del Proyecto
El repositorio incluye tres cuadernos de Jupyter, que reflejan las etapas principales del flujo de trabajo:

SHOP-ANALYSIS.ipynb: Exploración de datos y experimentación inicial.
MODELING-2.ipynb: Optimización y evaluación de modelos.
Deploy_model.ipynb: Despliegue del modelo final.
Descripción detallada de los cuadernos
SHOP-ANALYSIS.ipynb
Este cuaderno es el punto de partida del proyecto. Incluye:

Carga y exploración de datos:

Se analiza un conjunto de datos históricos que incluye ventas diarias por tienda, producto y categoría.
Visualización de tendencias, estacionalidad y patrones de ventas utilizando gráficos.
Ejemplo de visualizaciones generadas:

Gráficas de series temporales mostrando el comportamiento de las ventas diarias.
Análisis de correlaciones para identificar factores que afectan las ventas.
Preprocesamiento de datos:

Identificación y manejo de valores nulos.
Conversión de variables categóricas en variables numéricas (One-Hot Encoding).
Normalización de datos para garantizar que los modelos trabajen eficientemente.
Feature Engineering:

Generación de nuevas características relevantes:
Retardos (lags): Ventas de los días anteriores para capturar dependencias temporales.
Promedios móviles: Tendencias a corto y largo plazo de las ventas.
Días de la semana: Para capturar efectos estacionales.
Prueba inicial de modelos:

Se prueban dos enfoques principales:

LSTM (Long Short-Term Memory): Una red neuronal recurrente para series temporales.
XGBoost: Un modelo basado en árboles de decisión optimizados.
Se comparan métricas iniciales como RMSE (Root Mean Squared Error) y MAE (Mean Absolute Error).

Resultados:

LSTM: Generaliza mejor, pero tiene un alto costo computacional.
XGBoost: Menor costo computacional, con un rendimiento prometedor.
Conclusiones iniciales:

Se decide continuar optimizando el modelo XGBoost debido a su eficiencia y desempeño competitivo.
MODELING-2.ipynb
Este cuaderno se centra en:

Optimización de los hiperparámetros del modelo XGBoost utilizando Optuna.
Validación cruzada con series temporales (TimeSeriesSplit).
Entrenamiento del modelo final con todos los datos y generación de métricas definitivas.
Deploy_model.ipynb
Se implementa el modelo final con:

Uso de Modelbit para el despliegue.
Creación de funciones personalizadas para realizar predicciones fácilmente en nuevos datos.
Tecnologías Utilizadas
Lenguaje: Python
Bibliotecas:
Análisis de datos: pandas, numpy, matplotlib, seaborn
Modelado: xgboost, scikit-learn
Optimización: optuna
Despliegue: Modelbit

Ejecutar los cuadernos:

Ejecuta SHOP-ANALYSIS.ipynb para realizar el análisis exploratorio y preprocesamiento.
Continúa con MODELING-2.ipynb para optimizar los modelos y entrenar el modelo final.
Usa Deploy_model.ipynb para desplegar el modelo en un entorno de producción.
Predecir con el modelo:

Una vez desplegado, utiliza el modelo para realizar predicciones sobre nuevos datos cargados.
Resultados
El modelo final, optimizado con Optuna, alcanzó las siguientes métricas en la validación recursiva:

RMSE: 0.9494
MAE: 0.2390
RMSSE: 0.1406
Este modelo está diseñado para realizar predicciones de ventas a corto plazo con precisión y eficiencia.