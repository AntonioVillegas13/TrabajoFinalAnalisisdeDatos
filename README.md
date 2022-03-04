# Pulso político en 20 ciudades del Ecuador
1.- En esta rama pueden disponer de los scripts utilizados para realizar una recopilación de datos en tiempo real de la app de twitter por medio de su API de desarrollo, 
el analisis de los sentimientos de cada usuario, su almacenaje en una base de datos relacional(SQL SERVER) y su traslado a una base no relacional(MONGO DB)

![image](https://user-images.githubusercontent.com/74626067/156849886-4c309ae1-31bc-49be-9a6c-7255a7709245.png)

2.- A continuación, se presenta una visualización de los datos recopilados mediante uestra función/script en python almacenados en la base SQL server

![image](https://user-images.githubusercontent.com/74626067/156851115-3f77f7ef-07a6-447d-95ca-dd4f6bcdf91d.png)

3.- Mediante la porción de codigo indicada, realizamos la conexion en ambas bases, declaramos un variable con la instrucción
select que apunte a nuestra tabla en la BD SQL Server. Por parte de MongoDB, realizamos su conexión respectiva, creamos una base y una colección para almacenar nuestros datos. Mediante un for, recorremos esta, declarando una variable con formato json, recopilamos cada campo que contiene nuestro
cursor y lo vamos almacenando en cada clave del json, y, con un metodo de nuestra colección mongo db, insertamos el dato almacenado.

![image](https://user-images.githubusercontent.com/74626067/156852266-e536cb2f-2f31-489a-9e54-78ee00a2128b.png)

4.- Verificamos que el proceso se haya realizado con exito.

![image](https://user-images.githubusercontent.com/74626067/156852602-63f51af8-2608-45a9-9717-23dbe12dbe20.png)

