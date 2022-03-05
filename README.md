# Estado de COVID a nivel Mundial
En esa rama se explicara como se llegó a analizar las información, puesto que gracias a eso se opto por una fuente que es la Organización Mundial De la Salud, dado que en la fuente existe información valiosas para ser analizada, donde nos dan archivos CSV, en ese caso se tomo el archivo con información de todos los países en referencia al total de vacunas y los tipos.
![image](https://user-images.githubusercontent.com/98060370/156856407-fdceadf7-86c7-4131-98b0-2e4dce257d61.png)

## Explicación del Script  
### Json a CouchDB 

El script consiste en transformar un archivo CSV a un Json, puesto de que nos servirá para ir guardando en la base de datos CouchDB.

A continuación, se muestra la explicación del código fuente, como primero se exporta las librerías necesarias.

![image](https://user-images.githubusercontent.com/98060370/156856711-3e3e6711-e1b3-4691-a353-0aefa9f7020c.png)

En la siguiente imagen abrimos el archivo Json y lo codificamos, como observación es que el archivo Json debe encontrarse en la misma ruta donde este el código fuente.

![image](https://user-images.githubusercontent.com/98060370/156856738-c1a8b020-591f-48f0-b73a-ebf5aa91f065.png)

A continuación se realiza la conexión a la base de datos en nuestro caso a CouchDB, puesto de que es necesario conocer sus credenciales.

![image](https://user-images.githubusercontent.com/98060370/156856977-23be4ce0-614d-4d4c-be5e-cbe29f38c1b4.png)

Despues se crea un for donde la variable va a recorrer toda la documentación que se guardo en la variable myjson, donde toda la información se ira guardando, Sin embargo se creo unas excepciones en el caso de que exista un error.

![image](https://user-images.githubusercontent.com/98060370/156857192-138e861e-2f40-443e-aa30-20ebcc3fb07c.png)

Finalmente verificamos nuestra base de datos.

![image](https://user-images.githubusercontent.com/98060370/156857315-8aaae832-2b95-4398-bf3e-b92d62a6024f.png)

### CouchDB a MongoDB
Como primera parte importamos las librerías necesarias

![image](https://user-images.githubusercontent.com/98060370/156857648-16aeafe4-7c31-47c2-96c3-9175006155cb.png)

Luego realizamos la conexión de CouchDB y MongoDB utilizando las credenciales personales.

![image](https://user-images.githubusercontent.com/98060370/156857676-098496a7-874a-43cd-ab6b-701f56a917d6.png)


A continuación, apuntamos a la librería que queremos pasar a MongoDb a CouchDB.

![image](https://user-images.githubusercontent.com/98060370/156857708-265fb5a1-de3e-44d6-9f74-fe0c48a05c60.png)


Después creamos la base de datos y la colección para la base de Datos MongoDb.

![image](https://user-images.githubusercontent.com/98060370/156857725-0860f302-94c2-4518-9a7e-d32dcecc045d.png)

Luego se crea una función donde nos permita dar formato, dado que CouchDB tiene diferente formato con relación a MongoDB, teniendo en cuenta las nombres de las columnas de la base de datos a importar.

![image](https://user-images.githubusercontent.com/98060370/156857747-28248fe1-8984-4c56-aa66-549678d5c361.png)

Finalmente verificamos nuestra Base de Datos MongoDb
![image](https://user-images.githubusercontent.com/98060370/156857855-05c44eb3-2055-4cdc-85af-6a9bbc15696e.png)

## Análisis de datos recopilados

Para analizar la información se utilizó Power Bi puesto de que es un servicio de análisis de datos de Microsoft orientado a proporcionar visualizaciones interactivas y capacidades de inteligencia, permitiéndonos analizar los diferentes campos que tiene la base de datos para lograr resultados satisfactorios, brindando información organizada y estructurada por medio de graficas.

![image](https://user-images.githubusercontent.com/98060370/156858248-ace6f617-c5e0-4491-94ed-3a087243122e.png)

Finalmente se analiza los datos con el uso de la aplicación Power Bi con las diferentes funcionalidades y herramientas que tiene, en ese caso se analiza la información que se obtuvo de la fuente de la Organización Mundial de la Salud.
Se logra interpretar el total de vacunaciones que se tiene en cada país y los tipos de vacunas usadas, puesto de que es información importante para la sociedad, Sin embargo, se realiza un filtro por medio de los países para mejorar la búsqueda de información por países, Finalmente la información documentada es actualizada.

![image](https://user-images.githubusercontent.com/98060370/156858684-2c9dc7cc-8ce9-4a86-9f68-5c943abfa862.png)


![image](https://user-images.githubusercontent.com/98060370/156858698-29a85695-119c-46da-9d01-82600be087d9.png)






