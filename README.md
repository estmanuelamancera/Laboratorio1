Puedes abrir el notebook en Google Colab aquí: https://colab.research.google.com/drive/1XrlLjsHk9_Wyr7CvPzZhjuHke7vIsaNK?usp=sharing
# Análisis estadístico de la señal :
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

<img width="342" height="255" alt="image" src="https://github.com/user-attachments/assets/f6d1fb4e-4443-40e5-af04-1e1edc77decd" /> <br>
# CODIGO 

Para iniciar el primer fragmento de este código tiene como fin leer, procesar y representar una señal fisiológica (como un ECG) que proviene de PhysioNet.  Inicialmente, se establece Google Drive para tener acceso a archivos guardados en la nube, y se instala las liberías wfdb, que facilita la lectura de registros fisiológicos en los formatos.dat y.hea.  

 - plt.plot() : Encargada de dibujarla señal.
 - plt.xlabel() y plt.ylabel() : Colocan etiquetas en los ejes.
 - plt.grid() :Encargada de activar la cuadrícula para el gráfico.

Luego, se establece el camino hacia el archivo relevante, se carga a través de wfdb.rdrecord() y se muestra la señal completa utilizando wfdb.plot_wfdb().  Posteriormente, se obtiene información de la señal a través de record.p_signal, la cual se guarda como un arreglo de tipo NumPy que simboliza la amplitud de la señal a través del tiempo.

<img width="1059" height="490" alt="image" src="https://github.com/user-attachments/assets/757733c4-223a-451b-bb83-f67694cdb2c4" />
 Por otro lado en la parte de plt.figure, se hace la visualización general de la señal, la cual  grafica los primeros 1000 puntos en una fugura 12x4".
 - lighcoral: El color.
 - plt.show(): Para visualizar la señal.
   
# Cálculo de estadísticos descriptivos


# PROCEDIMIENTO
# Parte B

En la Parte B del laboratorio, una señal fisiológica fue producida experimentalmente por medio del generador de señales biológicas. Se empleó un sistema de adquisición de datos (DAQ) para obtenerlo, el cual fue conectado físicamente al PC por medio de USB y configurado con el controlador NI-DAQmx. El DAQ recibió la señal analógica del generador, la transformó a formato digital y la transfirió a MATLAB, donde se guardó en un archivo *.csv*. Posteriormente, la señal fue importada a Python para realizar análisis estadísticos y graficarla. Así, se calcularon los parámetros estadísticos obtenidos en la Parte A y se comparó la señal descargada de Physionet con la señal capturada usando el DAQ, lo que evidenció sus semejanzas y diferencias.

<img width="1024" height="768" alt="Diagrama de Flujo Árbol de decisiones Sencillo Verde (1)" src="https://github.com/user-attachments/assets/77a8eab6-c25d-4d99-92fb-3a21c1697ce2" />



![WhatsApp Image 2025-08-23 at 11 25 57 AM](https://github.com/user-attachments/assets/aa81cf54-221c-4e34-8ceb-925a94f26407) <br><br>


# CÓDIGO 
Este código permite leer el excel con los datos obtenidos del DAQ, separa la columna de tiempo y la de la señal, y desarrolla la gráfica de la señal tipo fisiologica. De permitiendo ver cómo cambia la amplitud de la señal con respecto al tiempo.  <br>
<img width="392" height="290" alt="image" src="https://github.com/user-attachments/assets/23dcd1fc-9551-435a-b613-5e877a89d81d" /><br>

en esta parte de calculan las estadísticas descriptivas de la señal registrada, es decir, la media, la desviación estándar, el coeficiente de variación y la curtosis. Los resultados se muestran en pantalla con cuatro decimales.<br>
<img width="371" height="261" alt="image" src="https://github.com/user-attachments/assets/692dcc6f-dd14-48d5-9b95-ce305b4db90f" /><br>
| ESTADISTICO     | VALOR   |
|-----------------|----------|
| Media          | 1.2197   |
| Desviación estandar | 0.4012   |
|Coeficiente de variación | 0,3289   |
| curtosis | 4,6892   |

<img width="818" height="228" alt="image" src="https://github.com/user-attachments/assets/cb4502c0-c4e9-4240-87a6-12990cca2d46" /><br><br>



continuando con la captura de las estadisticas continuamos con el histograma, que nos indica las veces que se repitieron los datos<br>
<img width="529" height="108" alt="image" src="https://github.com/user-attachments/assets/5a57b2c4-befb-4063-a3ab-f01d4931a72b" /><br>
<img width="884" height="588" alt="image" src="https://github.com/user-attachments/assets/c76755d9-d465-4082-864c-20ca8ea3dc45" />
<br>


para terminar con el analisis de la grafica obtenemos la funcion de probabilidad de la grafica que es un estima de como se podrian distribuir los datos.<br>
<img width="435" height="178" alt="image" src="https://github.com/user-attachments/assets/21530faa-7cbf-47b5-abbd-0e65300865fe" /><br>
<img width="875" height="589" alt="image" src="https://github.com/user-attachments/assets/b15a82bd-352d-4973-847d-0a8731ea4fc0" />
<br>


cumpliendo con el ultimo requerimiento de la guia, vamos a comparar la señal obtenida y analizada en la parte B con la señal incial (Parte A)<br>
<img width="836" height="216" alt="image" src="https://github.com/user-attachments/assets/69618b99-6ae7-47f1-a887-4fd32e2fadb9" /><br><br>
<img width="828" height="945" alt="image" src="https://github.com/user-attachments/assets/4a2902d1-f0bc-4898-b9cc-91500acbbb0c" /><br>
Al comparar la Parte A "PhysioNet" con la Parte B "señal generada", se observa que la grafica A está más cercana a 0 ademas presenta picos más marcados, lo que refleja mejor el comportamiento real de un ECG. En cambio, la grafica B muestra valores más altos y estables, con menos variaciones bruscas, lo que indica que es una señal más suavizada y sencilla en comparación con la real.<br><br>

# PROCEDIMIENTO 
# Parte C
Para finalizar nuestra practica vamos a emplear **SNR** (signal to noise ratio), la relación señal ruido se trata de una medida que pone en comparación la fuerza de señal util  (calidad) de una señal a diferencia con el nivel de ruido presente, es decir,Un SNR alto significa que la señal es clara y sobresale respecto al ruido, por el contrario si el SNR de la señal es muy bajo, nos indica que el ruido hace demasiada interferencia respecto a la señal y afecta la trasmisión e interpretación de esta.

Empleando la señal obtenida en el inciso B, vamos a contaminarla con __ruido gaussiano__ variaciones pequeñas y aleatorias, **ruido de impulso** picos fuertes y repentinos y __Ruido tipo artefacto__ errores que se producen por un sistema que trasmita la señal. y calcularemos sus respectivos SNR.<br>

<img width="340" height="257" alt="image" src="https://github.com/user-attachments/assets/d8838ae3-3446-4327-ae1e-b40e708fc34e" /> <br>


# CÓDIGO
Este código calcula la relación entre una señal original y su versión con ruido, mostrando qué tan clara es la señal frente a la interferencia.Comparando la fuerza de la señal con la del ruido<br>
<img width="386" height="169" alt="image" src="https://github.com/user-attachments/assets/176ae783-5a47-481b-b560-bb2fea4bd26c" /><br>
<img width="1280" height="591" alt="image" src="https://github.com/user-attachments/assets/4fa66aa8-f2c0-474f-a671-98086d4c3d1d" />


Este código agrega ruido gaussiano a la señal original de ECG para simular cómo se vería en condiciones menos ideales, grafica la señal,y analiza su SNR permitiendo comparar la forma original con la señal afectada por el ruido.<br>
<img width="509" height="180" alt="image" src="https://github.com/user-attachments/assets/fbb7ed14-8402-44c3-9190-de14ad26d58e" /> <br>
<img width="828" height="736" alt="image" src="https://github.com/user-attachments/assets/a3c0184d-c815-4639-99c0-ca1d787aaeb3" /> <br>

continuamos agregando ruido de impulso a la señal original de ECG, graficando la señal,e igualmente analizando su SNR permitiendo permitiendo observar cómo cambia su forma al verse afectada por este tipo de ruido.<br>
<img width="515" height="200" alt="image" src="https://github.com/user-attachments/assets/562ac372-78d1-4091-87ed-eaeed5dd9131" /> <br>
<img width="828" height="723" alt="image" src="https://github.com/user-attachments/assets/5ddfc238-db87-402f-a658-b619e4ec11ef" /><br>

continuamos agregando el ruido de artefacto a la señal original, y realizamos el mismo procedimiento que las señales anteriores.<br>
<img width="551" height="190" alt="image" src="https://github.com/user-attachments/assets/d5a38829-b050-4396-9967-df86f8f61560" /><br>
<img width="828" height="746" alt="image" src="https://github.com/user-attachments/assets/e9d29fe7-4410-484b-bf2c-3a7769e97343" /><br>

Finalmente este codigo nos permitira visualizar los resultados obtenidos <br>
<img width="297" height="94" alt="image" src="https://github.com/user-attachments/assets/021aa4b3-099d-4241-811b-d1e58d8bfb08" /> <br>
<img width="427" height="136" alt="image" src="https://github.com/user-attachments/assets/34b68f47-f4b6-4b87-b786-984f063fa227" /><br>
<img width="828" height="1472" alt="image" src="https://github.com/user-attachments/assets/1a705506-370d-4e8f-b297-8f598a5cdb26" />















