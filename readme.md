# Análisis del Cambio Electoral en Olot (2023)

## Descripción del Proyecto

Este proyecto tiene como objetivo analizar el cambio electoral ocurrido en las elecciones municipales de 2023 en la ciudad de Olot. Dicho cambio consistió en el paso de la CUP de la cuarta fuerza a la segunda, estando incluso a punto de alcanzar la alcaldía.

Para analizar este cambio, tratamos de entender los factores demográficos y sociológicos que llevaron a él, estudiando las fortalezas y debilidades de los principales partidos, y muy principalmente de la CUP. Igualmente, intentamos, mediante el método de la inferencia ecológica, descubrir las transferencias de voto ocurridas, si es que hubo.

## Dataset

El análisis se realizó utilizando un dataset organizado por secciones censales que contiene las siguientes variables:

- **SECCION**: cada sección censal.
- **RMH**: renta media por hogar.
- **PES**: porcentaje de población con estudios superiores.
- **HAB**: número de habitantes.
- **LENGUA**: lengua predominante (catalán o castellano) en cada sección censal:
  - 1. Catalán.
  - 2. Castellano.
  - 3. Mixto.
- **15-19**: habitantes entre 15 y 19 años.
- **20-29**: habitantes entre 20 y 29 años.
- **30-39**: habitantes entre 30 y 39 años.
- **40-49**: habitantes entre 40 y 49 años.
- **50-59**: habitantes entre 50 y 59 años.
- **60-69**: habitantes entre 60 y 69 años.
- **70-MAS**: habitantes de 70 o más años.
- **HOMBRES**: número de varones.
- **MUJERES**: número de mujeres.
- **JUNTS19**: votos a Junts en 2019.
- **ERC19**: votos a ERC en 2019.
- **PSC19**: votos a PSC en 2019.
- **CUP19**: votos a CUP en 2019.
- **ECP19**: votos a ECP en 2019.
- **ABSTENCIÓN19**: abstención en 2019.
- **JUNTS23**: votos a Junts en 2023.
- **ERC23**: votos a ERC en 2023.
- **PSC23**: votos a PSC en 2023.
- **CUP23**: votos a CUP en 2023.
- **ECP23**: votos a ECP en 2023.
- **ACTIVEM23**: votos a Activem en 2023.
- **ARA-PL23**: votos a ARA PL en 2023.
- **VOX23**: votos a VOX en 2023.
- **ABSTENCION23**: abstención en 2023.

## Estructura del Proyecto

1. **Carga y exploración del dataset**
   - Exploración inicial de los datos para familiarizarnos con las variables y la estructura del dataset.
   
2. **Análisis exploratorio de datos (EDA)**
   - Visualización de las distribuciones de las variables clave.
   - Cálculo de los cambios en el voto entre 2019 y 2023.
   - Visualización de los cambios en el voto para identificar patrones.

3. **Clustering y Segmentación**
   - Aplicación de técnicas de clustering para segmentar las secciones censales según características demográficas y cambios en el voto.
   - Análisis de los clusters para identificar diferencias y similitudes entre los grupos.

4. **Análisis de Regresión Multinivel**
   - Modelización de los cambios en el voto utilizando técnicas de regresión multinivel, teniendo en cuenta la estructura jerárquica de los datos.
   - Validación cruzada y exploración de modelos alternativos para evaluar la robustez de los resultados.

5. **Inferencia Ecológica**
   - Aplicación del método de inferencia ecológica utilizando la librería `lphom` para estimar las transferencias de voto entre partidos.
   - Análisis detallado de las transferencias de voto hacia la CUP.

6. **Conclusiones**
   - Resumen de los hallazgos clave del análisis.
   - Reflexión sobre las implicaciones políticas y sociológicas del cambio electoral en Olot.

## Modelos y Métodos

- **Regresión Multinivel**: Utilizado para modelar los cambios en el voto y explorar las influencias de las variables demográficas.
- **Clustering**: Aplicado para segmentar las secciones censales y facilitar el análisis comparativo.
- **Inferencia Ecológica**: Implementada con la librería `lphom` para analizar las transferencias de voto.
- **Modelos de Machine Learning**: Se exploraron modelos como `XGBoost`, `Random Forest`, `Elastic Net`, y otros, para predecir cambios en el voto, aunque con resultados variados en términos de eficacia.

## Resultados

Los resultados sugieren que los factores demográficos, especialmente la lengua predominante, han jugado un papel significativo en el cambio electoral observado. La inferencia ecológica reveló importantes transferencias de voto hacia la CUP, que fue clave para su ascenso en las elecciones de 2023.

## Conclusiones

El proyecto demuestra la importancia de analizar los cambios electorales desde múltiples perspectivas, utilizando tanto técnicas tradicionales de análisis como métodos más avanzados de machine learning e inferencia ecológica. Este enfoque holístico proporciona una visión más completa de los factores que influyen en los resultados electorales.

## Requisitos

- Python 3.x
- Librerías: `pandas`, `statsmodels`, `sklearn`, `xgboost`, `rpy2`, `matplotlib`, `seaborn`
- R con `lphom`

## Ejecución

Para ejecutar el análisis completo, sigue estos pasos:

1. **Preparación del entorno**: Instala las dependencias necesarias.
2. **Carga del dataset**: Carga el dataset y realiza una exploración inicial.
3. **Análisis y modelización**: Ejecuta los scripts de análisis exploratorio, clustering, regresión y machine learning.
4. **Inferencia ecológica**: Utiliza el script correspondiente para realizar la inferencia ecológica con la librería `lphom`.

## Contacto

Para cualquier consulta sobre este proyecto, puedes contactar con el autor a través de [tu email o contacto].

