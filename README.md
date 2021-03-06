<h1 align="center"><b>FIFA12 Ultime Team</b></h1>

Football API es una prueba que pretende construir y consumir una replica de la api FIFA 12 Ultime Team permitiendo hacer busqueda de jugadores y equipos.

## Comenzando 馃殌

Para probar el funcionamiento de nuestro proyecto, podemos realizar la descarga del repositorio ubicado en Github.

* Estando ubicados en el GitHub seleccionaremos la opci贸n **Code** el cual se encuentra en un recuadro de color verde, el siguiente paso sera seleccionar la opci贸n **Download ZIP** y este iniciara con la descarga del archivo.

## Despliegue

Cuando la descarga del archivo haya finalizado haremos la descompresi贸n y nos debera quedar una carpeta con el nombre **Football API**

### Pre-requisitos 馃搵

Para poner en marcha el proyecto nos ayudaremos de una consola, en mi caso utilizo el sistema operativo Ubuntu 20.04 pero las instrucciones son las mismas para otros sistemas.

Desde la consola abriremos la ubicaci贸n de la carpeta que acabamos de descomprimir, esto lo podemos lograr abriendo la carpeta y luego con clic derecho seleccionamos **Abrir en una terminal**

El siguiente paso sera abrir el directorio llamado api; primero comprobaremos que la ruta de nuestra consola sea similar a la siguiente:

```
/football-api$
```
Para abrir el directorio en menci贸n escribiremos en la consola **cd api** seguido de un enter. Nuestra nueva ruta debe ser similar a la siguiente.

```
football-api/api$
```

### Instalaci贸n 馃敡

Para que la api pueda ser visible desde un navegador debemos crear un entorno, ya que esta se encuentra en un docker y no permite ser visualizada.

* El primer paso sera construir nuestros contenedores, esto lo haremos con el siguiente comando:

```
sudo docker-compose up --build
```

<img src="https://github.githubassets.com/images/icons/emoji/unicode/26a0.png?v8" width="13px"> **En caso de ser requerida una contrase帽a la introduciremos**

* Cuando haya terminado, abrimos una nueva terminal y ejecutamos los siguientes comandos:

```
sudo docker ps
```
_En la informaci贸n mostrada buscaremos la columna **NAMES**  y veremos en nombre de nuestro contenedor, en nuestro caso es **football-api-1**_

* El siguiente comando sera:
```
sudo docker exec -it football-api-1 bash
```
_El comando anterior nos creara una nueva ruta en la consola, ahora pondremos el ultimo comando para terminar de construir nuestra api._

```
npm run extract
```

_El comando anterior recopilara toda la informaci贸n que utilizaremos en nuestra api y al mismo tiempo la escribir谩 en una base de datos la cual nos permitir谩 el manejo de la informaci贸n_ 
<img src="https://github.githubassets.com/images/icons/emoji/unicode/26a0.png?v8" width="13px"> **Este paso puede tomar un tiempo** <img src="https://github.githubassets.com/images/icons/emoji/unicode/23f3.png?v8" width="13px">

## Ejecutando las pruebas 鈿欙笍

Ahora para poder ver la api en funcionamiento solo debemos abrir el navegador de internet de nuestra preferencia, en el campo de la URL escribiremos lo siguiente:

```
http://localhost:8080/
```

Para iniciar una b煤squeda en el campo de **Search** pondremos una palabra o letra clave para obtener los resultados de  los jugadores, como opciones podemos filtrar las b煤squedas por orden ascendente o descendente.
<img src="https://github.com/steven-cruz/cuemby-test/blob/master/docs/img/Selecci%C3%B3n_062.png?raw=true">
<img src="https://github.com/steven-cruz/cuemby-test/blob/master/docs/img/Selecci%C3%B3n_061.png?raw=true">

Para poder ver todos los jugadores pertenecientes a determinado equipo debemos cambiar la opci贸n de **Name** por **Team** e introducir el nombre del equipo por completo seguido de enter.
<img src="https://github.com/steven-cruz/cuemby-test/blob/master/docs/img/Selecci%C3%B3n_063.png?raw=true">

Para obtener mas informaci贸n sobre cada jugador podemos presionar el bot贸n **See more** ubicado en la tarjeta de cada uno.
<img src="https://github.com/steven-cruz/cuemby-test/blob/master/docs/img/Selecci%C3%B3n_064.png?raw=true">

Una vez terminadas las pruebas en la api es necesario destruir el contenedor creado; para esto realizaremos los siguientes pasos:
1. Cerraremos la consola donde ejecutamos el comando **npm run extract**
2. En la consola donde ejecutamos el comando **sudo docker-compose up 鈥揵uild** presionaremos **Ctrl + c** para detener los procesos, seguido a esto utilizaremos el siguiente comando para remover los contenedores.
```
sudo docker-compose down -v
```


## Autors 鉁掞笍

**Juan Portilla**  
* [LinkedIn](https://www.linkedin.com/in/jdpa352/)
* [Twitter](https://twitter.com/jdavid357)

**Kevin Castro**
* [LinkedIn](https://www.linkedin.com/in/kevin-brandown-castro-/)
* [Twitter](https://twitter.com/ccali_k)
---