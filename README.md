# Proyecto-13-Bootcamp

•	Objetivo: Análisis de comportamiento de miembros de gimnasio por medio de clustering

•	Librerías importadas: pandas, seaborn, numpy, matplotlib, sklearn (preprocesado, modelos y métricas), scipy (linkage/dendrogram).

•	Carga de datos: lee el CSV gym_churn_us.csv (ruta: '/datasets/gym_churn_us.csv').

•	Análisis Exploratorio de Datos:

o	describe() e info() para resumen y revisión de nulos.

o	groupby('Churn').mean() para comparar medias entre quienes se van/quedan.

o	Histogramas y countplots para variables clave: Lifetime, Contract_period, Age, Avg_class_frequency_total, Partner, Promo_friends.

o	Matriz de correlación visualizada con heatmap.

•	Clasificación (predicción de churn):

o	X = todas las columnas menos 'Churn', y = 'Churn'.

o	Split train/test 80/20 con stratify.

o	Modelos entrenados: LogisticRegression (solver='liblinear') y RandomForestClassifier.

o	Evaluación: accuracy, precision y recall impresos para ambos modelos.

•	Clustering:

o	Estandarización con StandardScaler aplicada a X (sin 'Churn').

o	Dendrograma jerárquico usando linkage(method='ward').

o	KMeans con n_clusters=5 (n_init=10), añade columna 'cluster_km' al DataFrame.

o	Cálculo de medias por clúster y visualizaciones de distribuciones por clúster.

o	Cálculo de tasa de churn por clúster.

•	Conclusiones y recomendaciones finales del revisor sobre perfiles de riesgo y posibles estrategias de retención.
