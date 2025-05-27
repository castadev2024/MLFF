# MLFF
Segmenting consumer preferences in vending machines for offer personalization using K-Means

## Video que describe la solución

https://www.youtube.com/watch?v=PKL2oVIETZU

## Agrupacion_vector.ipynb 

El propósito del este archivo es segmentar las preferencias de los consumidores en máquinas expendedoras para la personalización de ofertas utilizando el algoritmo de agrupamiento K-Means. Se procesa un conjunto de datos de pedidos de clientes, aplica preprocesamiento y se hace una reducción de dimensionalidad (PCA), evaluando y seleccionando el número óptimo de clusters, y luego asigna a los clientes a grupos basados en sus preferencias de ingredientes. 

También incluye métodos para generar recomendaciones personalizadas de productos para cada cluster, comparando los perfiles de los grupos con un conjunto de productos. El flujo de trabajo tiene como objetivo permitir mejores recomendaciones de productos y una personalización de ofertas más efectiva para diferentes segmentos de clientes, basados en sus patrones de compra.

## App.ipynb 

A travez de este archivo se implementar y demostrar el proceso de segmentación de preferencias del consumidor utilizando el algoritmo de agrupamiento K-Means.
1. Cargar y preprocesar los datos de consumidores de las máquinas expendedoras.
2. Aplicar K-Means para segmentar los clientes en función de sus preferencias.
3. Analizar y visualizar los segmentos resultantes.
4. Extraer conclusiones sobre cómo personalizar ofertas en las máquinas expendedoras basándose en estos segmentos.

## Data_preparation_LSTM.ipynb

- Carga datos del historial de pedidos de clientes e información de los productos, incluidos los vectores de ingredientes.
- Analiza cada pedido de los clientes, convirtiendo la información del carrito en vectores binarios de ingredientes para cada pedido.
- Combina estos vectores para representar la presencia de cada ingrediente por pedido.
- Agrega los datos procesados en un DataFrame donde cada cliente está asociado con una lista de vectores de pedidos.
- Guarda el resultado en un nuevo archivo CSV (clientes_vectores_binarios.csv) para su uso posterior en el modelado.

## Extracion_ventana_temporal_5.ipynb

- Carga los datos de transacciones desde anonymized_transactions_full.csv.
- Limpia los datos eliminando las filas con valores faltantes.
- Ordena los datos de transacciones por cliente y por marca de tiempo.
- Agrupa los datos por cliente (FF_CUSTOMER_ID) para:
- Contar el número de pedidos por cliente.
- Agrupar los pedidos de cada cliente en una lista con los detalles del pedido (ID del pedido, contenido del carrito, marca de tiempo).
- Analiza y visualiza la distribución del número de pedidos por cliente usando descripciones estadísticas, histogramas y diagramas de caja.
- Calcula los porcentajes de clientes con al menos 2, 3, 5, 10 o 20 pedidos.
- Filtra el conjunto de datos para conservar solo los clientes con 5 o más pedidos y guarda este subconjunto como clientes_5_o_mas_pedidos.csv.
- Proporciona ejemplos y visualizaciones para un análisis más detallado de estos clientes frecuentes.

## LSTM.ipynb

Implementa y optimiza un model LSTM para modelar las secuencias de compras de los clientes en máquinas expendedoras, permitiendo recomendaciones personalizadas de ofertas basadas en el historial de compras.
