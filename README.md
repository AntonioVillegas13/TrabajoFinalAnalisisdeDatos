# Eventos o Noticias Mundiales
En este apartado se muestra la recoleccion de datos de fuentes como tweeter y kaggle, para un analisis de eventos como el SuperBowl y el Terrorismo a nivel mundial. 
Base de datos de kaggle usada: https://www.kaggle.com/START-UMD/gtd


#Tema SuperBowl ------------------------------------------------------------------------------------------------------

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

#Tema Terrorismo ------------------------------------------------------------------------------------------------------

Primero usamos una base de datos que extraemos de kaggle https://www.kaggle.com/START-UMD/gtd

![image](https://user-images.githubusercontent.com/74798975/156852351-f158c1ea-c192-4db5-bcf7-9963fec5529f.png)

Ahora lo importamos en nuestro MYSQL
Para ello creamos un schema y en tablas importamos nuestro .csv haciendo click derecho en "Table Data Import Wizard"

![image](https://user-images.githubusercontent.com/74798975/156852444-640a2cb1-d7ba-4b6c-94a4-4d1e6754981e.png)

Buscamos nuestra base de datos que descargamos de Kaggle y lo importamos dando en next:

![image](https://user-images.githubusercontent.com/74798975/156852572-96d7ceac-c6fc-4d71-a88e-5f15f6ad6be0.png)
![image](https://user-images.githubusercontent.com/74798975/156852668-2b4939c6-54a5-423f-a803-678ee0d2dab4.png)

Una vez importado revisamos los datos en nuestro MYSQL con una linea de comando en el script de la base de datos, por ejemplo:

![image](https://user-images.githubusercontent.com/74798975/156852891-1a2f2855-7a18-4ae5-b79f-60ade3915e13.png)

Ahora una vez con datos en nuestro MYSQL usaremos el script mysql2mongodb.ipynb para enviar nuestros datos de MYSQL a mongoDB.
Primero en esta seccion pondremos los datos de nuestro localhost para el mysql. (host = 'localhost', user = 'tu_usuario', password = 'tu_contraseña')

![image](https://user-images.githubusercontent.com/74798975/156853343-6437c492-0200-4d41-aa25-f2a8b04c2606.png)

En esta seccion realizamos una pequeña consulta de la tabla que importamos en el mysql para conprobar que si esta hecha la conexion. ("SELECT * FROM tu_tabla", connections)

![image](https://user-images.githubusercontent.com/74798975/156853542-a407e0c8-7f5b-4598-9b9a-e7b6b560e28e.png)

Ejecutamos el script normalmente y listo. Revisaremos nuestro mongoDB y comprobaremos que nuestra base se ha exportado.

![image](https://user-images.githubusercontent.com/74798975/156853702-cfb04bed-aad7-4a6f-88da-1a970b0450a9.png)


#Importar datos de mongoDB a PowerBi ------------------------------------------------------------------------------------------------------

Una vez importado los distintos datos en las diferentes bases de datos como fueron de couchDB y MYSQL, ahora los datos de mongoDB los usaremos para realizar analisis con ayuda de PowerBI. (La conexion entre el PowerBi y MongoDB se encuentran en el readme principal)

En PowerBi importamos los datos desde el ODBC que ya debemos haber instalado y configurado.
![image](https://user-images.githubusercontent.com/74798975/156853901-3d9819d9-d9b9-432d-9799-f890e6c6b870.png)

Escogemos el DNS con el que se conectaran el mongoDb y el PowerBi para usar los datos que se encuentran en mongoDB. (En mi caso el DNS se llama Adrian)

![image](https://user-images.githubusercontent.com/74798975/156853972-22e659fa-802e-4e6f-8375-50de2f6dcaaf.png)

!!Recuerda que para que funcione el conector DNS debes ejecutar lo siguiente como administrador, pues es el que lee las bases de datos que se encuentre en tu mongoDB:

![image](https://user-images.githubusercontent.com/74798975/156854211-4aa41540-b819-420e-a241-1d44cebe1aee.png)
![image](https://user-images.githubusercontent.com/74798975/156854296-2d45ac8e-3c7d-4c30-8127-91fb5a892dc1.png)

Ahora solo escogemos las bases de datos de las cuales queremos realizar graficas para poder realizar un buen analisis de cada una de ellas.

![image](https://user-images.githubusercontent.com/74798975/156854394-8a5c241d-d6a2-4824-9127-1e49bc9e63a4.png)

Algunos ejemplos de graficas basadas en los datos que hemos usado para este ejemplo:

#Superbowl

![image](https://user-images.githubusercontent.com/74798975/156854545-2e9fd7a8-0e58-4f39-b1a7-575373a7651b.png)

#Terrorismo

![image](https://user-images.githubusercontent.com/74798975/156854592-6764b4ca-72f8-42fd-8786-aa64560f157b.png)
![image](https://user-images.githubusercontent.com/74798975/156854744-7673a24f-2521-4360-88cd-70566d69f140.png)








