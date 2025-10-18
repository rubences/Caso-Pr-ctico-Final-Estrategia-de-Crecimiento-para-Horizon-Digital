# Caso Práctico Final: Estrategia de Crecimiento para "Horizon Digital"
Empresa: Horizon Digital Contexto: Eres el nuevo Científico de Datos de "Horizon Digital", una empresa de e-commerce que vende una variedad de productos electrónicos. La dirección quiere lanzar una nueva estrategia para el próximo año fiscal y te ha encargado realizar un análisis de 360 grados de los datos de los clientes y las ventas para fundamentar sus decisiones.

proyecto Objetivo: Desarrollar un análisis integral que incluya análisis exploratorio de datos (EDA), modelos predictivos (regresión y clasificación), segmentación de clientes (clustering) y pronóstico de ventas (series temporales).

## VISUALIZACIÓN DE DATOS Y ANÁLISIS EXPLORATORIO DE DATOS (EDA) 📊

https://umber-year-57965818.figma.site/

## Requisitos del Proyecto
Lenguaje: Python
Librerías: pandas, numpy, matplotlib, seaborn, scikit-learn, statsmodels
Entorno: Jupyter Notebook
## Estructura del Proyecto

- data/: Contendrá los datos originales y procesados.
- notebooks/: Contendrá los Jupyter Notebooks con el análisis y modelado.
- src/: Contendrá el código fuente para la preparación de datos, modelado y evaluación.
- requirements.txt: Listado de dependencias del proyecto.
## Dataset

Se te proporciona un archivo ecommerce_data.csv con los siguientes campos:

CustomerID: Identificador único del cliente.
Age: Edad del cliente.
Gender: Género del cliente.
AnnualIncome: Ingresos anuales del cliente (en miles de USD).
TimeOnSite: Tiempo promedio que el cliente pasa en el sitio web por sesión (minutos).
ItemsInCart: Número promedio de artículos que el cliente deja en el carrito.
LastPurchaseAmount: Monto de la última compra (USD).
TotalSpending: Gasto total histórico del cliente (USD).
IsSubscribed: Si el cliente está suscrito al boletín de noticias (1=Sí, 0=No).
LastPurchaseDate: Fecha de la última compra.
## Misión 1: Entendiendo el Negocio (Análisis Exploratorio de Datos) 📊
La dirección necesita una visión general de la situación actual. Quieren entender quiénes son sus clientes y cómo se comportan.

Tu Tarea:

Carga y Limpia los Datos: Realiza una inspección inicial del dataset, maneja los valores nulos (si los hay) y asegúrate de que los tipos de datos son correctos.
Análisis Descriptivo: ¿Cuál es la distribución de edad, género e ingresos de los clientes?
Análisis de Comportamiento:
Crea un gráfico de dispersión (scatter plot) para visualizar la relación entre TimeOnSite y TotalSpending. ¿Pasan más tiempo los clientes que más gastan?
Usa un diagrama de caja (boxplot) para comparar el TotalSpending entre los clientes suscritos y los no suscritos. ¿Los suscriptores gastan más?
Conclusión Inicial: Escribe un breve párrafo resumiendo tus 2-3 hallazgos más importantes del EDA.

## Misión 2: Prediciendo el Valor del Cliente (Regresión) 💰
El equipo de finanzas quiere predecir cuánto gastará un nuevo cliente a lo largo de su vida. Esto les ayudará a determinar cuánto pueden invertir en adquirir nuevos clientes.

Tu Tarea:

Prepara los Datos: Selecciona las características relevantes (Age, AnnualIncome, TimeOnSite, ItemsInCart) para predecir TotalSpending.
Entrena un Modelo de Regresión: Implementa un modelo de Random Forest Regressor, ya que suele ser robusto.
Evalúa el Modelo: Utiliza el RMSE (Error Cuadrático Medio Raíz) para medir el error de tu modelo.
Interpreta los Resultados: Identifica las características más importantes (feature_importances_) del modelo. ¿Qué factor influye más en el gasto total de un cliente?

## Misión 3: Identificando Clientes Potenciales (Clasificación) ✅
El equipo de marketing quiere enfocar su próxima campaña de suscripción en los clientes con mayor probabilidad de suscribirse al boletín.

Tu Tarea:

Define el Problema: Tu variable objetivo es IsSubscribed. Las características a usar son Age, TimeOnSite y TotalSpending.
Entrena un Modelo de Clasificación: Implementa un modelo de Regresión Logística. No olvides escalar tus características (StandardScaler).
Evalúa el Modelo: Crea una matriz de confusión para analizar los resultados. Calcula la precisión (accuracy) y el recall.
Conclusión de Marketing: Basado en tu modelo, ¿qué perfil de cliente (Age, TimeOnSite, TotalSpending) tiene más probabilidades de suscribirse? Explica brevemente por qué el recall podría ser una métrica importante para este caso.

## Misión 4: Creando Campañas Personalizadas (Clustering) 🎯
La dirección cree que no todos los clientes son iguales. Quieren identificar grupos de clientes para crear campañas de marketing personalizadas.

Tu Tarea:

Prepara los Datos para Clustering: Selecciona las columnas AnnualIncome y TotalSpending.
Encuentra el Número Óptimo de Clústeres: Usa el Método del Codo (Elbow Method) con el algoritmo K-Means para determinar el mejor número de segmentos de clientes.
Aplica K-Means: Ejecuta el algoritmo con el k óptimo y asigna cada cliente a un clúster.
Crea las "Personas": Analiza los centroides de cada clúster y crea un perfil para cada uno. Por ejemplo:
VIP: Altos ingresos, alto gasto.
Leales: Ingresos medios, gasto medio-alto.
Potenciales: Altos ingresos, bajo gasto.
Recomendación Estratégica: Sugiere una acción de marketing específica para el clúster "Potenciales".

## Misión 5: Pronosticando las Ventas Futuras (Series Temporales) 📈
Finalmente, el equipo de operaciones necesita un pronóstico de ventas para gestionar el inventario y la logística para el próximo año.

Tu Tarea:

Prepara la Serie Temporal: Agrupa los datos de LastPurchaseAmount por mes a partir de la columna LastPurchaseDate para crear una serie temporal de ventas mensuales.
Analiza la Serie: Visualiza la serie y descomponla en tendencia y estacionalidad. ¿Hay algún patrón visible?
Entrena un Modelo de Pronóstico: Implementa un modelo SARIMA para capturar los patrones de la serie.
Genera un Pronóstico: Predice las ventas para los próximos 12 meses.
Visualiza el Futuro: Crea un gráfico que muestre los datos históricos y el pronóstico de 12 meses, incluyendo los intervalos de confianza.

Debes entregar un único Jupyter Notebook que contenga las cinco misiones. El notebook debe estar bien estructurado, con títulos claros para cada misión, código funcional y celdas de Markdown con tus explicaciones, interpretaciones y conclusiones para cada tarea.

Al final del notebook, incluye una sección de "Recomendaciones Estratégicas Generales" donde resumas tus hallazgos de las cinco misiones y ofrezcas 3 recomendaciones clave a la dirección de "Horizon Digital".

# ¡Buena suerte y feliz análisis de datos! 🚀
