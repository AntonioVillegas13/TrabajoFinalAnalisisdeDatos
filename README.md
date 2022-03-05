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

_En este caso solamente descargamos los documentos y dejamos a un lado los videos para no cargar nuestro sistema_



















