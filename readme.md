# Análisis del Cambio Electoral en Olot (2023)

## Descripción del Proyecto

Este proyecto tiene como objetivo analizar el cambio electoral ocurrido en las elecciones municipales de 2023 en la ciudad de Olot. Dicho cambio consistió en el paso de la CUP de la cuarta fuerza a la segunda, estando incluso a punto de alcanzar la alcaldía.

Para analizar este cambio, tratamos de entender los factores demográficos y sociológicos que llevaron a él, estudiando las fortalezas y debilidades de los principales partidos, y muy principalmente de la CUP. Igualmente, intentamos, mediante el método de la inferencia ecológica, descubrir las transferencias de voto ocurridas, si es que hubo.

## Dataset

El análisis se realizó utilizando un dataset organizado por secciones censales que contiene las siguientes variables:

| Variable        | Descripción                                                      |
|-----------------|------------------------------------------------------------------|
| **SECCION**     | Cada sección censal.                                             |
| **RMH**         | Renta media por hogar.                                           |
| **PES**         | Porcentaje de población con estudios superiores.                 |
| **HAB**         | Número de habitantes.                                            |
| **LENGUA**      | Lengua predominante (catalán o castellano) en cada sección censal: |
|                 | 1. Catalán.                                                      |
|                 | 2. Castellano.                                                   |
|                 | 3. Mixto.                                                        |
| **15-19**       | Habitantes entre 15 y 19 años.                                   |
| **20-29**       | Habitantes entre 20 y 29 años.                                   |
| **30-39**       | Habitantes entre 30 y 39 años.                                   |
| **40-49**       | Habitantes entre 40 y 49 años.                                   |
| **50-59**       | Habitantes entre 50 y 59 años.                                   |
| **60-69**       | Habitantes entre 60 y 69 años.                                   |
| **70-MAS**      | Habitantes de 70 o más años.                                     |
| **HOMBRES**     | Número de varones.                                               |
| **MUJERES**     | Número de mujeres.                                               |
| **JUNTS19**     | Votos a Junts en 2019.                                           |
| **ERC19**       | Votos a ERC en 2019.                                             |
| **PSC19**       | Votos a PSC en 2019.                                             |
| **CUP19**       | Votos a CUP en 2019.                                             |
| **ECP19**       | Votos a ECP en 2019.                                             |
| **ABSTENCION19**| Abstención en 2019.                                              |
| **JUNTS23**     | Votos a Junts en 2023.                                           |
| **ERC23**       | Votos a ERC en 2023.                                             |
| **PSC23**       | Votos a PSC en 2023.                                             |
| **CUP23**       | Votos a CUP en 2023.                                             |
| **ECP23**       | Votos a ECP en 2023.                                             |
| **ACTIVEM23**   | Votos a Activem en 2023.                                         |
| **ARA-PL23**    | Votos a ARA PL en 2023.                                          |
| **VOX23**       | Votos a VOX en 2023.                                             |
| **ABSTENCION23**| Abstención en 2023.                                              |

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
   - De todo el trabajo anterior podemos extraer varias conclusiones. Estas, dado que nos enfrentamos a un fenómeno tan complejo y potencialmente volátil como es el comportamiento electoral, tienen necesariamente un margen de incertidumbre, que nos lleva a mantener una necesaria cautela. No obstante, creemos que hay varias realidades que se pueden señalar:

     - La CUP ha demostrado tener una base electoral leal, lo cual, combinado con el gran aumento de la abstención en las elecciones de 2023, constituye una parte importante de su éxito.

     - En distinta medida, la CUP ha conseguido atraer votantes de las fuerzas nacionalistas hegemónicas. Es un fenómeno interesante, dada la distancia puramente ideológica existente entre ambos grupos (en especial en lo referente a Junts). Esto sugiere, en el ámbito local, una campaña y unos candidatos bien ajustados a la realidad olotina. En una clave más nacional, la CUP puede haber conseguido atraer en Olot a votantes decepcionados con la deriva posterior al 1 de octubre de 2017; algo que, ciertamente, no se ha producido en otros lugares, lo que nos obliga a ser especialmente cuidadosos con esta hipótesis.

     - Los datos indican que la CUP también ha conseguido atraer a votantes que se abstuvieron en 2019, lo que puede indicar un potencial de crecimiento, así como cierta capacidad de ilusionar a personas no especialmente interesadas por la política.

     - En el proyecto hemos dado importancia a la variable lengua, ya que suele ser un buen predictor del comportamiento electoral. La CUP ha conseguido un ascenso especialmente importante en las zonas catalanoparlantes, algo que es a la vez una fortaleza y una potencial debilidad: fortaleza en tanto que puede continuar erosionando a los partidos nacionalistas hegemónicos; debilidad en lo que respecta a lo que sería esperable en una formación situada tan a la izquierda, que debería ser capaz de superar las barreras étnico-lingüísticas.

     - De todo lo anterior, se deduce una enseñanza no por repetida menos importante: en las zonas en las que existe una disputa por la cuestión nacional, esta lo atraviesa todo, lo que hace que el análisis, necesariamente, vaya más allá del eje izquierda-derecha; lo que implica que el análisis preste atención a los indicadores asociados a la pertenencia nacional o étnica.

## Modelos y Métodos

- **Regresión Multinivel**: Utilizado para modelar los cambios en el voto y explorar las influencias de las variables demográficas.
- **Clustering**: Aplicado para segmentar las secciones censales y facilitar el análisis comparativo.
- **Inferencia Ecológica**: Implementada con la librería `lphom` para analizar las transferencias de voto.
- **Modelos de Machine Learning**: Se exploraron modelos como `XGBoost`, `Random Forest`, `Elastic Net`, y otros, para predecir cambios en el voto, aunque con resultados variados en términos de eficacia.

## Contacto

Para cualquier consulta sobre este proyecto, puedes contactar con el autor a través de awfuentes76@gmail.com.
