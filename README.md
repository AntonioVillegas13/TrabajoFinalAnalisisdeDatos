# Eventos o Noticias Mundiales
En este apartado se muestra la recoleccion de datos de fuentes como tweeter y kaggle, para un analisis de eventos como el SuperBowl y el Terrorismo a nivel mundial. 
Base de datos de kaggle usada: https://www.kaggle.com/START-UMD/gtd


#Tema SuperBowl

->Consideraciones:

En esta seccion las claves son proporcionadas por twitter de manera que puedas realizar el twitter-scraper, debes conseguir estas claves antes de hacer la practica.

![image](https://user-images.githubusercontent.com/74798975/156850819-767b177a-f2f2-40c7-9d0a-a128e1bc3be3.png)

En esta seccion para conectar al couchDB debes usar tu ususario y contraseña ('http://usuario:contraseña@localhost:5984/')

![image](https://user-images.githubusercontent.com/74798975/156850905-235998e5-b084-427f-a501-fddc2fe00280.png)

Para extraer datos de twitter usamos el script Twitter2Couch2Mongo.ipynb de manera que jalamos los datos, con un track con palabras clave como "SuperBowl" y "NFL".
![image](https://user-images.githubusercontent.com/74798975/156850147-5d7351bb-1fec-4e3a-9743-f9ace4cfab6e.png)

Una vez extraido suficientes tweets para los analisis correspondientes observaremos que se han almacenado en nuestro couchDB, para el ejemplo se han recolectado mas de 5 mil tweets:

![image](https://user-images.githubusercontent.com/74798975/156850271-9ec6bd16-7561-4aa5-bb1f-da7f700afb5d.png)

Ahora para enviar los datos de mongoDB a couchDB, usamos el mismo script en la parte baja se encuentra un apartado con el script que usaremos para enviar la informacion de couchDB a mongoDB.

![image](https://user-images.githubusercontent.com/74798975/156851101-8b8f1306-a6f9-4aa3-a2ae-ed5d292fe64b.png)

En este apartado especificamos que datos queremos extraer de cada tweet, en este caso algunos campos son el nombre del usuario, el texto, su localizacion, etc.

![image](https://user-images.githubusercontent.com/74798975/156851196-c1fcf853-b5f1-4585-aaef-b9d28d0649d3.png)

Una vez ejecutado el script los datos habran sido exportados a tu mongoDB.

![image](https://user-images.githubusercontent.com/74798975/156851328-dbec5d23-74a2-4d51-8847-16ee1efc8c69.png)
