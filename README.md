# TrabajoFinalAnalisisdeDatos
Trabajo final de la materia de análisis de datos  donde se hizo web scrapping y se implemento dataset para interpretar los datos mediante el analisis


## En este apartado se explicara a breves rasgos el apartado de videojuegos online

primero realizaremos la busqueda en el buscador especifico con las palabras claves que mejor describan nuestra busqueda.

Link del data set con formato JSON
<https://epnecuador-my.sharepoint.com/:u:/g/personal/antonio_villegas_epn_edu_ec/EUb2qZGGiqhEvkD6DpWycyABUxy1r-jOIQiiKZYg4ekXUg?e=P0jOSS>


![image](https://user-images.githubusercontent.com/88470677/156864997-04753022-a13c-443d-a000-677647dc312b.png)

dentro de este buscador podremos encontrar varios data  sets  que podremos descargar , alguno son de paga, pero si se llega a encontrar  data set gratis.
![image](https://user-images.githubusercontent.com/88470677/156865176-5b872ec6-599d-4948-b03f-e28429cb6ae1.png)

ahora, dependiendo de la platafarma de la cual obtengamos los data sets  podremos llegar a descargar csv, excel o json. Estos podremos irlos moviendo entre los distintas bases de datos para posteriormente implementarlo dentro del power bi.

![image](https://user-images.githubusercontent.com/88470677/156865220-88ea9f43-3f28-41df-b6e9-9890f836ca40.png)


ahora aprovechando que uno de los data set lo obtuvimos como json podremos subirlo ya se subiendo al mongoDB para luego conectar el mongoDB al  powe bi, o subirlo de manera directa.

![image](https://user-images.githubusercontent.com/88470677/156865408-c489ef07-f533-4523-999d-9d3d7f61fc5e.png)


Con nuestros datos cargados en el powe bi ya podremos empezar a realizar los diferentes analisis para interpretar los datos como informacion de valor 
![image](https://user-images.githubusercontent.com/88470677/156865429-03ca80c5-2e32-4357-881f-d72936130c49.png)

Ahora a partir de estos datos podremos ir construyendo graficas que nosayuden a contar los analisis que vayamos sacando de los datos extraidos.
![image](https://user-images.githubusercontent.com/88470677/156865590-4eec6caf-07a1-428a-b77e-8e5de38acaa4.png)


---
para el data set de csv podremos primero pasarlo a una base de datos como sqllite

![image](https://user-images.githubusercontent.com/88470677/156865645-07c3245e-8435-4a47-94ea-e13efac8da9d.png)

y luego solo tendremo que conectar esta base de adtos con ODBC dentro de power bi.
![image](https://user-images.githubusercontent.com/88470677/156865673-5353269c-3c64-406f-b481-7d2d1b177708.png)


