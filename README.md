# Análisis estadístico de la señal 
  # DESCRIPCIÓN
En este repocitorio se realizó el analisis de selañes biomédicas utilizando tanto datos adquiridos por bases de datos y señales generadas experimentalmente. 
Por lo tanto se inicio la descarga un señal fisiologica, importandola en Python para su graficación y calculos de parametros estadisticos. Por otro lado, se obtuvo una señal gracias al Osiloscopio,capturandola por el DAQ y se relaciono sus caracteristicas con la señal inicial. Además, se determino la influencia del ruido en las señales atraves del calculo de la relacion Señal-Ruido (SNR) y analizando sus efectos sobre la señal. 

   # OBJETIVOS 
 
1. Elegir, importar y analizar señales fisiológicas para su procesamiento estadístico en Python.
2. Crear una señal fisiológica en un laboratorio, captarla con la DQ y analizar sus propiedades estadísticas.

3. Utilizando funciones predefinidas en Python y métodos manuales, comparar las propiedades estadísticas de señales simuladas con las de señales reales.
  # PROCEDIMIENTO 
  
# Parte A
En esta parte inicial se realizo la descarga de una señal fisiologica desde la base de datos *PhysioNet*, asegurándose de que tuviera el tiempo necesario para calcular los parámetros estadísticos requeridos. Por lo tanto, Se importó la señal en Python y se usaron bibliotecas como matplotlib para representarla gráficamente. Esto marcó el comienzo del análisis estadístico de la señal, utilizando herramientas informáticas que facilitan la descripción de sus rasgos más relevantes.



# Parte B
Continuamos el desarrollo de nuestra practica obteniendo una señal fisiologica por medio del *generador de señales*, y capturandola con ayuda del DAQ, este proceso requirio la conexión adecuada del generador y la entrada de DAQ, y con ayuda de la aplicación " " se pudo hacer conversión de señal analogica a Digital,finalmente los datos de esta señal se guardaron en un excel, lo que facilito su grafica y analisis de esta. 

| ESTADISTICO     | VALOR   |
|-----------------|----------|
| Media          | 1.2197   |
| Desviación estandar | 0.4012   |
|Coeficiente de variación | 0,3289   |
| curtosis | 4,6892   |

