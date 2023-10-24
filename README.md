# Primera entrega - OPAIN
En esta primera entrega se exponen los resultados de la limpieza de datos basada en el EDA enviado anteriormente y se evaluan supuestos de regresion para evaluar la viabilidad del proyecto. Como entregables se tienen los siguientes archivos:

## Data
Es la carpeta de resultados y archivos de lectura con los siguientes archivos:
- **Aeropuertos.csv, hdi.csv y pib.csv**: Archivos de fuentes externas que integran informacion de continente, HDI y PIB respectivamente.
- **clean_flights.csv y clean_sales.csv**: Archivos limpios de vuelos y ventas partiendo de los Exceles originales enviados por OPAIN, atendiendo a las dimensiones de calidad aprendidas en la clase.
- **muelle.parquet**: Archivo de datos para regresion agrupados por vuelo, cuyo valor de ventas esta representado por una porcion de las ventas del muelle.
- **marca{1 a 10}.parquet**: Archivos de datos para regresion agrupados por vuelo, cuyo valor de ventas esta representado por una porcion de ventas de la marca respectiva.
- **ols_report.txt**: Reporte de resultados de aplicar OLS a los datos de muelle, luego de aplicar transformaciones y supuestos de regresion.

## Notebooks de entregables
En la carpeta raiz los notebooks se ejecutan en orden secuencial de la siguiente manera:

0. **PRIMERA ENTREGA.ipynb**: Notebook que describe de manera general la entrega hecha.
1. **1_Limpieza_datos_comerciales.ipynb**: Limpia datos comerciales (ventas) con base en las dimensiones de calidad.
2. **2_Limpieza_datos_operativos.ipynb**: Limpia datos operativos (vuelos) con base en las dimensiones de calidad.
3. **3_Union_datos_operativos_y_comerciales.ipynb**: Une los datos operativos y comerciales agrupados por hora y muelle para generar datos de regresion por vuelo con base en las ventas del muelle.
4. **4_Modelo_regresion.ipynb**: Evaluacion de supuestos de regresion, entrenamiento de modelo de regresion y OLS, y evaluacion de metricas.

### (ANEXOS)

5.  **ANNEXO_0_union_de_datos_operativos_y_comerciales_por_marca.ipynb**: Une los datos operativos y comerciales agrupados por hora y muelle para generar datos de regresion por vuelo con base en las ventas de cada marca, generando un archivo por marca.
6.  **ANNEXO_1_a_regression_por_marca_random_forest.ipynb**: Experimento preliminar de regresion con random forest, con marcas separadas.
7.  **ANNEXO_1_b_regression_por_muelle_random_forest.ipynb**: Experimento preliminar de regresion con random forest, con todas las marcas como una sola unidad de muelle.
