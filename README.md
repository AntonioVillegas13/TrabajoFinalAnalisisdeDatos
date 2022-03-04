# Recopilacion de datos (Scraping):
- Kaggle       - OMS
- Twitter      - GitHub
- Tiktok       - Twitter
- Web          - Statista
- Youtube      - DataSet
     

### Integrantes
- Adrian Chicaiza
- Alexander Tupiza
- Jean Fuentes
- Eduardo Farinango
- Antonio Villegas

## Ruta planteada
![Ruta](https://raw.githubusercontent.com/AntonioVillegas13/TrabajoFinalAnalisisdeDatos/main/image.png)

# Pasos previos
## Conexion entre MongoDB y Power Bi
### Requisitos
Instale BI Connector y configúrelo para conectarse a su conjunto de réplicas.
Link: https://www.mongodb.com/try/download/bi-connector
Descargue e instale Visual C++ Redistributable para Visual Studio 2015 .
Link: https://www.microsoft.com/en-us/download/details.aspx?id=48145
1- Descargar e Intalar todos los requisitos necesarios y tener abierto MongoDB y Power BI
![image](https://user-images.githubusercontent.com/98060370/156851585-bf377644-b9a8-4119-9f39-4cf8ec39240c.png)

2- Nos dirigimos al disco local 'C' a la carpeta de Mongodb, donde encontraremos una subcarpeta nombrada Connector for BI, donde dentro de esa carpeta encontraremos otra carpeta nombrada 2.14 y otra 'bin', puesto de que en esa carpeta encontraremos 4 archivos donde ejecutaremos como administrador el que tenga el nombre de 'mongosqld'
![image](https://user-images.githubusercontent.com/98060370/156852253-67c40c86-0fd4-4a76-8439-0e36d05898ab.png)

3- Luego de haber ejecutado administrador nos brindara un cmd, con información valiosa como lo es la IP y el puerto.
![image](https://user-images.githubusercontent.com/98060370/156852384-298ff6f4-46b1-4a0c-8826-f005beffd86f.png)

4 – Después nos dirigimos al buscador de Windows y colocamos ‘Orígenes de datos ODBC de 64 bits’ según el procesador de cada maquina en la que se vaya a realizar, Abrimos y nos dirigimos al DNS del sistema para agregar el driver.
![image](https://user-images.githubusercontent.com/98060370/156853280-cd021e3f-4e3e-49e9-9e8d-d861f63ee73d.png)

5- Posteriormente damos en agregar y elegimos el driver en nuestro caso el Unicode.
![image](https://user-images.githubusercontent.com/98060370/156853428-683b0282-cc6c-4c13-9ec1-b4b69b6c5546.png)

6- Después nos mostrara un ventana para colocar la información correspondiente según la IP y el Puerto.
![image](https://user-images.githubusercontent.com/98060370/156853593-ab13f087-18cc-4729-b5d4-f3e100358f1d.png)

![image](https://user-images.githubusercontent.com/98060370/156853756-3122d5fd-567a-4de1-be90-a5bb0a982e6d.png)

7- A continuación nos dirigimos a Power BI a cargar los datos por medio el conector OBDC, dado que nos va a dar a elegir el DNS creado.
![image](https://user-images.githubusercontent.com/98060370/156854066-a479b120-304a-43be-a3ca-a74abbde93aa.png)

8- Finalmente iniciamos en Windows y luego nos mostrara una ventana con todas las bases de datos que se tenga en el MongoDB, para luego cargar y analizar. 

![image](https://user-images.githubusercontent.com/98060370/156854232-592ff4ed-0de6-4063-8546-5d88c392cf88.png)


Descargue e instale el controlador ODBC de MongoDB BI Connector .
Link: https://github.com/mongodb/mongo-bi-connector-odbc-driver/releases/

[Generar API keys de twitter](https://developer.twitter.com/en) registrarse como desarrollador y realizar la petición de las KEY's_

Instalación de [Python](https://www.python.org/) y [Project Jupyter](https://jupyter.org/) Lab o si prefiere [Anaconda](https://www.anaconda.com/products/individual) que ya trae paquetes pre instalados.


# Obetivo General
- Entender los métodos que existen para la recolección      de datos de diferentes fuentes alojadas en el Internet que permitan mediante su análisis escalar en la pirámide de conocimiento  hasta su punto más alto para generar sabiduría basados en una arquitectura Data Lake.	

# Obetivos Especificos
-          Definir una estructura Data Lake adecuada para la recopilación de datos.
-          Definir un tema de estudio que cumpla con los requerimientos del caso.
-           Tratar los datos recolectados con el software adecuado en cada nivel.
-          Alojar los datos recolectados utilizando gestores de bases de datos relacionales y no relacionales.
-          Concentrar los datos recolectados en MongoDB.
-          Importar bases de datos que recibieron tratamiento a PowerBI.

# Temas
## [Pulso Político en 20 ciudades principales de Ecuador](https://github.com/AntonioVillegas13/TrabajoFinalAnalisisdeDatos/tree/1.Pulso-político-en-20-ciudades-principales-de-Ecuador)
## Estado de COVID a nivel mundial
## Juegos en línea por países
## [El aborto](https://github.com/AntonioVillegas13/TrabajoFinalAnalisisdeDatos/tree/4.-Tema-definido-por-el-estudiante)
## [Eventos o noticias mundiales](https://github.com/AntonioVillegas13/TrabajoFinalAnalisisdeDatos/tree/5.-Eventos-o-Noticias-Mundiales)


