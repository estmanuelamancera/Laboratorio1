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



# CODIGO 
<img width="392" height="290" alt="image" src="https://github.com/user-attachments/assets/23dcd1fc-9551-435a-b613-5e877a89d81d" />
Este código permite leer el excel con los datos obtenidos del DAQ, separa la columna de tiempo y la de la señal, y desarrolla la gráfica de la señal tipo fisiologica. De permitiendo ver cómo cambia la amplitud de la señal con respecto al tiempo.
![WhatsApp Image 2025-08-23 at 11 25 57 AM](https://github.com/user-attachments/assets/aa81cf54-221c-4e34-8ceb-925a94f26407)


<img width="371" height="261" alt="image" src="https://github.com/user-attachments/assets/692dcc6f-dd14-48d5-9b95-ce305b4db90f" />
en esta parte de calculan las estadísticas descriptivas de la señal registrada, es decir, la media, la desviación estándar, el coeficiente de variación y la curtosis. Los resultados se muestran en pantalla con cuatro decimales.
| ESTADISTICO     | VALOR   |
|-----------------|----------|
| Media          | 1.2197   |
| Desviación estandar | 0.4012   |
|Coeficiente de variación | 0,3289   |
| curtosis | 4,6892   |

<img width="818" height="228" alt="image" src="https://github.com/user-attachments/assets/cb4502c0-c4e9-4240-87a6-12990cca2d46" />


<img width="529" height="108" alt="image" src="https://github.com/user-attachments/assets/5a57b2c4-befb-4063-a3ab-f01d4931a72b" />
continuando con la captura de las estadisticas continuamos con el histograma, que nos indica las veces que se repitieron los datos
<img width="884" height="588" alt="image" src="https://github.com/user-attachments/assets/6aa2010d-5dbd-458e-a0c1-1c384a017c17" />

<img width="435" height="178" alt="image" src="https://github.com/user-attachments/assets/21530faa-7cbf-47b5-abbd-0e65300865fe" />
para terminar con el analisis de la grafica obtenemos la funcion de probabilidad de la grafica que es un estima de como se podrian distribuir los datos.
<img width="875" height="589" alt="image" src="https://github.com/user-attachments/assets/4fe123ee-81fc-4eee-9ec6-927917aa3a94" />

<img width="445" height="87" alt="image" src="https://github.com/user-attachments/assets/dada731e-8eea-42bd-8530-a6167f7547c9" />
cumpliendo con el ultimo requerimiento de la guia, vamos a comparar la señal obtenida y analizada en la parte B con la señal incial (Parte A)
<img width="836" height="216" alt="image" src="https://github.com/user-attachments/assets/69618b99-6ae7-47f1-a887-4fd32e2fadb9" />
<img width="828" height="945" alt="image" src="https://github.com/user-attachments/assets/4a2902d1-f0bc-4898-b9cc-91500acbbb0c" />
Al comparar la Parte A "PhysioNet" con la Parte B "señal generada", se observa que la grafica A está más cercana a 0 ademas presenta picos más marcados, lo que refleja mejor el comportamiento real de un ECG. En cambio, la grafica B muestra valores más altos y estables, con menos variaciones bruscas, lo que indica que es una señal más suavizada y sencilla en comparación con la real.













