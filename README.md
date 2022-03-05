# Data Lake with PowerBI
_Proyecto de fin de semestre en el cual se creará un DATA LAKE enfocado en la recopilación de datos mediante websacraping, API Keys, páginas que permiten realizar webscraping._

## Objetivo del apartado 🚀

_Se recopilaran datos de la red social Twitter utilizando coordenadas y la palabra clave ‘aborto’, así mismo de TikTok con  [tiktok-scraper](https://github.com/drawrowfly/tiktok-scraper/tree/develop) utilizando la misma palabra clave y websacrping  especializado para esta red social y para finalizar  utilizaremos la página web [Apify](https://apify.com/) para realizar scraping a YouTube._

### Recopilación de datos de Twitter
_Para iniciar este proceso es necesario tener las API Keys que Twitter nos proporciona y con la ayuda de la página web [Boundingbox](https://boundingbox.klokantech.com/) conseguiremos las coordenadas de las cuidades que deseamos solicitar datos._
_KEY's_
![image](https://user-images.githubusercontent.com/75056800/156851331-11242016-3ca1-4f8d-98a9-b974f9cae7f0.png)

_Coordenadas de BouBoundingbox_
![image](https://user-images.githubusercontent.com/75056800/156851460-c3c1ee40-7678-49e6-8c3f-e753057f2862.png)

_Una vez que cumplimos estos requisitos procederemos mediante scripts de Python a extraer los datos enviándole los datos conseguidos anteriormente hay que tomar en cuenta también que se debe instalar [Tweepy](https://docs.tweepy.org/en/stable/) en nuestras librerías_
![image](https://user-images.githubusercontent.com/75056800/156852001-fc99ff04-3aee-4502-8e05-7c741852a3b9.png)

_Podemos observar que iniciamos importando nuestras librerías tanto de CouchDB acompañado de otras librerías necesarias para este paso, se creara una clase que mediante  tweepy va empezar a extraer los datos que necesitamos y los va a ir guardando en nuestra base de datos, como paso siguiente vamos a crear nuestra conexión con CouchDB utilizando los métodos que nos brinda para este caso, le enviamos la ruta del servidor en este caso el Localhost apuntando al puerto 5984 juto al usuario y contraseña registrados al momento de la instalación._

![image](https://user-images.githubusercontent.com/75056800/156852737-14696bde-dc0b-4339-88ea-9b5d0656d286.png)

_Dentro de estas líneas de código podemos ver que se encuentra una variable que va a guardar nuestra clases que recibe como parámetros las Keys de Twitter, una vez listos mediante el método filter podemos enviarle nuestras coordenadas seleccionadas y la palabra clave. El script empezara a buscar la extracción de los datos._

![image](https://user-images.githubusercontent.com/75056800/156856402-bfc57dd1-7056-4980-a389-620f0872abbd.png)

_Este proceso se va a ver reflejado en CouchDB despues de haberlo realizado con varias coordenadas._

![image](https://user-images.githubusercontent.com/75056800/156856502-771caa9d-6251-439d-91b9-7bf8bd7efca9.png)

_Para continuar extraeremos datos de TikTok utilizando tiktok-scraper utilizando una línea de código que insertaremos en CDM o terminal del sistema operativo utilizado apuntando a la carpeta donde se va a guardar la información_

![image](https://user-images.githubusercontent.com/75056800/156857035-5cb6c188-82f2-4a30-bf46-ea43b1d23ab8.png)

_Este método de scraping nos permite a mas de conseguir la información en formato json csv también noes permite descargar los videos de los usuarios utilizando -d_

![image](https://user-images.githubusercontent.com/75056800/156857262-9f9b864b-ae78-42d0-9488-6bd9fb39d711.png)

_En este caso solamente descargamos los documentos y dejamos a un lado los videos para no cargar nuestro sistema._

_Ahora vamos a visitar [Apify](https://apify.com/) que después de registrarnos nos va a permitir realizar web sacraping a YouTube_

![image](https://user-images.githubusercontent.com/75056800/156859715-4bf43284-cb87-4fb6-993e-0f40983a0e08.png)

_Como podemos observar esta página nos permite ingresar una palabra clave y el número máximo de documentos que esperamos conseguir, damio clic en iniciar y nos indicara el proceso de nuestra tarea._

![image](https://user-images.githubusercontent.com/75056800/156859888-f16dca56-b81b-4366-9f80-4f967ba6c1df.png)

_Una vez terminado el proceso nos indicara lso datos que recolectamos dentro de una archivo json o csv y otros formatos y lo descargamos.
![image](https://user-images.githubusercontent.com/75056800/156860048-7f84ab14-f979-44bd-abcd-adca6cff0275.png)


_Estos datos dentro de documentos o bases de datos tienes que ser concentrados en MongoDB para esto utilizaremos otros scripts uqe nos permitiran extraexlos de las BD de marea sistematica, para los procesos que como resultado nos entregaron archivos json o csv utilizaremos primero el SGBD MySQL Workbench._

_Utilizaremos el wizard para poder importar los documentos y eliminaremos las columnas que no deseamos para poder concentrar los datos de Tiktok._

![image](https://user-images.githubusercontent.com/75056800/156860830-0ced4c03-7bd0-409b-b9d9-f23b832d790f.png)

![image](https://user-images.githubusercontent.com/75056800/156860910-636fcf7b-8b09-4963-8dab-5e981ac848e4.png)

_Una vez seleccionadas las columnas que nos van a servir para nuestro proyecto guardamos y verificamos la carga, tenemos una BD abortos base que contiene 2 tablas con la información necesaria_

![image](https://user-images.githubusercontent.com/75056800/156861167-70e7b25c-2c88-4670-9407-f5d7a6b4c902.png)


_Para poder implementar el documento que obtuvimos de YouTube scraping utilizaremos XAMPP que nos da el ingreso a PhpMySQL_

![image](https://user-images.githubusercontent.com/75056800/156861521-f0975801-451e-47f4-9376-de0873a4680c.png)

_Observamos que una vez iniciado el servidor apache podremos iniciar el servicio SQL ahora importaremos nuestro archivo json utilizando el método anterior y podremos ver nuestros datos en esta SGBD _

![image](https://user-images.githubusercontent.com/75056800/156861706-a50050c4-5262-49c1-9bfa-6440457b9cc6.png)

## Importación de datos a MongoDB

_Para este proceso utilizaremos 2 scripts que nos permitiran conectarnos tanto a CouchDB y a SQL_

_De CouchDb a MongoD_

_ Para iniciar cargaremos nuestros controladores y realizaremos nuestras conexiones con los respetivos servidores dándoles los nombres necesarios en cada SGBD_

![image](https://user-images.githubusercontent.com/75056800/156862228-17074f58-c91d-421f-a8d3-b0231bcc6cff.png)

_La conexión se ha realizado con éxito y ya tenemos un nombre de base de datos para guardar mediante un método que recorre todo el documento procederemos a pasa nuestra información._

![image](https://user-images.githubusercontent.com/75056800/156862551-5357998d-4512-46aa-b4bc-78c26eb06883.png)


_Como veremos en la siguiente imagen tenemos las mismas bases dedatos en CouchDB y MongoDB_

![image](https://user-images.githubusercontent.com/75056800/156862607-9a094a2d-ec16-4031-92fd-16f392189b4d.png)


_Para pasar lod datos desde MySQL y PhpMyadmin utilizaremos un script parecido pero en esta ocasión crearemos un dataframe con la ayuda de Pandas que será codificado y enviado a MongoDB_

![image](https://user-images.githubusercontent.com/75056800/156862740-a4334c65-ac7b-45bc-91b9-5b04c7e596b2.png)

_En la primera parte de nuestro script creamos las conexiones tanto para SGBD SQL 






































