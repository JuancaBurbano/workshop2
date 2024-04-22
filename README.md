# README ABOUT THE WORKSHOP 2

## Introduction 

Para este pryecto se nos pido la realizacion de una fusion entre dos distintos tipos de datos, los cuales fueron proporcionados por el docente, uno de estos estaba en formato csv, y el otro tenimos que insertarlo a una base de datos. Todo esto de forma automatizada mediante la herramienta AIRFLOW

A todo esto se le realizo un proceso de limpieza, tambien un proceso de analisis, incluido a esto, tambien se le realizo un proceso de automatizaciòn.

El estado de este proyecto es casi terminado, debido a que no se cumplio con el ultimmo requisito que fue subir a google drive nuestros datos finales mediante la API de google drive, pero de resto tenemos todo funcionando de manera automatizada hasta el punto de guardar los datos finales en una base de datos.

## Herramientas

Para este proyecto lo principal que se utilizo fue docker, debido a que corrimos airflow mediante contenedores ya que por el sistema operativo windows no podemos correrlo.
Tambien utilizamos python claramente para poder realizar codigo.
Varias librerias de python que mas adelante seran explicadas de como se utilizaron, para mas informacion buscar en la seccion instalaciòn.
El gestor de bases de datos, Postgres.
Y Power BI para poder visualizar estos datos

## Content of the project
Este proyecto/workshop se basa en 2 carpetas que contienen subcarpetas. Las dos pricnipales son airflow_first_dag, y la otra donde hacemos los notebooks llamada Notebooks.Tambien dentro de este proyecto encontraras los requirements que son todo lo que vas a necesitar para correr este proyecto, tambien debes crear un archivo Json que contentenga tus credenciales para acceder a la base de datos de postgres, porque en esto proyecto existia uno pero por el gitignore solicitado por el docente no es posible mostrarlo.
Ahora, vamos a ver cual es el contenido de las dos carpetas principales comenzando por airflow_first_dag:
Dentro de esta tenemos 3 subcarpetas, un docker compouse y un readme para correr el docker. Asi que procedamos a describir cada una de ellas para que entiendas como funcionan y que funcion cumplen.
Dentro de la primera subcarpeta llamada dags, tendras el workshop_dag, que es la carpeta que contendra todo el contenido para el flujo de airflow, dentro de ella existe, etl.py y workshop_dag.py que son los archivos que nos ayudaran a y se complementaran entre si a la hora de correr el flujo, en etl tenemos todas las funciones que van a llevar acabo este flujo, y en el workshop_dag, es donde nosotros llamamos a esas funciones para ponerlas en un "entorno" airflow, donde en este se espesifica, los arguments, los das, el flujograma, etc..
Ahora tenemos una carpeta llamada logs, que tendran que crear ustedes mismo tambien al igual que credentials.json, ya que este esta dentro del gitignore, y es donde van a estar los logs que va a sacar cada una de las tareas que correremos mas adelante.
Por ultimo esta la carpeta comodin plugins, que yo en este caso la decidi utilizar como carpeta que me guardara los archivos que yo necesitara para correr el proyecto, aqui encontraras todos los csv que hacen posible que este proyecto tenga datos, y en esta misma carpeta debes crear 2 credentials, uno que sea de la siguinte manera:
```
{
    "host" : "host.docker.internal",
    "user" : "",
    "password" : "",
    "database" : ""  
}

```
Alli vas colocando tus credenciales y en el segundo ya colocas las mismas credenciales para conectarte a tu base de datos local.
Y listo eso es todo lo que tienes que saber sobre como esta compuesto este proyecto.

## Instalation and configuration
Para la instalacion es muy sencillo y el profeso de configuracion para que puedas correr el proyecto en este caso mi workshop2 es demasiado facil ya que es un proceso autimatizado. 
Lo primero que debes hacer es instalar todos los requierments dentro del proyecto, todas las librerias que ves ahi debes instalarlas, entonces como haces esto, sencillo, abres una terminal con la direccion del proyecot y escribes lo siguiente:
```
pip install -r requirements.txt

```
Listo ya teneindo todas las dependencias y tambien las librerias que se van a usar solamente debes crear los credentials que te mostre en la anterior sección.

Ahora viene otra parte de instalación en este caso el programa docker si es que no lo tienes instalado, lo puedes instalar mediante el siguinete link: https://www.docker.com/products/docker-desktop/

Tambien debes tener instalado el gestor postgress y haber configurado su instalacion, si aun no lo tienes puedes instalarlo en el siguiente link:  https://www.postgresql.org/download/ 
Habiendo configurado este gestor debes crear la base de datos workshop2 y dentro de ella la tabla grammys, para poder insertar los datos a esta tabla y luego traerlos. Este proceso lo haces en uno de los notebooks en la carpeta Notebooks.
Ahora, despues de que ya has abierto docker, procedemos a correr el docker compouse, dentro de la carpeta airflow_first_dag esta otro readme con la informacion detallada de lo que debes hacer.

Si quieres realizar y ver los edas que se le realizaron a cada uno de los datasets, pues dirigete a la carpeta notebooks que cada uno de estos son jupyter Notebooks, una manera de correr codigo por celdas, y procede a correr cada celda en orden.

Ya que tienes todas estas partes hechas es hora de correr el dag, si ya ingresaste a localhost:8080 debes ver que te aparecen muchos das y que el primero se llama "dag_workshop" inicialo. Despues de esto ingresa a este dag para que puedas ver los graficos.
Despues de esto lo que debes hacer es correr el dag, ¿Como lo haces? arriba a la izquierda no tan arriba esta un boton de play, dale click ahi y mira como la automatizacion de airflow corre el proyecto.

## Dashboard

Para ver el dashboar debes ingresar aqui : **[Dashboard](https://github.com/JuancaBurbano/workshop2/blob/main/airflow_first_dag/plugins/workshop2.pdf)**.

## Reporte
Para poder ver el reporte que he creado sobre este proyecto puedes verlo en el siguiente link: https://docs.google.com/document/d/1NBlA778qiSLdZA64eNcdaWKpzHigMIywle_AJxlxTkw/edit?usp=sharing 
## Contacto
Mi correo es el siguinete por si deseas hacerme una consulta: camilitoburher17@gmail.com
