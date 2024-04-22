# README ABOUT THE WORKSHOP 2

## Introduction 

For this project we were asked to perform a fusion between two different types of data, which were provided by the teacher, one of these was in CSV format, and the other we had to insert into a database. All this in an automated way using the AIRFLOW tool

A cleaning process was carried out on all of this, as well as an analysis process, including this, an automation process was also carried out.

The status of this project is almost finished, because the last requirement was not met, which was to upload our final data to Google Drive through the Google Drive API, but for the rest we have everything working in an automated way up to the point of saving the data. final data in a database.

## Tolds

For this project, the main thing used was docker, because we ran airflow through containers since we cannot run it due to the Windows operating system.
We also clearly use Python to be able to code.
Several python libraries that will later be explained how they were used, for more information look in the installation section.
The database manager, Postgres.
And Power BI to be able to visualize this data

## Content of the project
This project/workshop is based on 2 folders containing subfolders. The two main ones are airflow_first_dag, and the other one where we make the notebooks called Notebooks. Also within this project you will find the requirements that are everything you will need to run this project, you must also create a Json file that contains your credentials to access the postgres database, because in this project there was one but due to the gitignore requested by the teacher it is not possible to show it.
Now, let's see what is the content of the two main folders starting with airflow_first_dag:
Inside this we have 3 subfolders, a docker compouse and a readme to run docker. So let's proceed to describe each of them so that you understand how they work and what function they fulfill.
Within the first subfolder called dags, you will have the workshop_dag, which is the folder that will contain all the content for the airflow flow, within it there is etl.py and workshop_dag.py, which are the files that will help us and will complement each other. If at the time of running the flow, in etl we have all the functions that are going to carry out this flow, and in the workshop_dag, is where we call those functions to put them in an airflow "environment", where it is specified, the arguments, the days, the flowchart, etc.
Now we have a folder called logs, which you will also have to create yourself, as well as credentials.json, since this is inside gitignore, and it is where the logs that each of the tasks that we will run later will be. .
Finally, there is the wildcard plugins folder, which in this case I decided to use as a folder that will save the files that I will need to run the project, here you will find all the csv that make it possible for this project to have data, and in this same folder you must create 2 credentials, one that is as follows:
```
{
    "host" : "host.docker.internal",
    "user" : "",
    "password" : "",
    "database" : ""  
}

```
There you enter your credentials and in the second you enter the same credentials to connect to your local database.
And that's it, that's all you need to know about how this project is composed.

## Instalation and configuration
The installation is very simple and the configuration process so you can run the project, in this case my workshop2, is too easy since it is an automated process.
The first thing you must do is install all the requirements within the project, all the libraries that you see there you must install, so how do you do this, simple, you open a terminal with the address of the project and write the following:
```
pip install -r requirements.txt

```
Ready, having all the dependencies and also the libraries that are going to be used, you only have to create the credentials that I showed you in the previous section.

Now comes another installation part, in this case the docker program, if you do not have it installed, you can install it through the following link: https://www.docker.com/products/docker-desktop/ 

You must also have the postgress manager installed and have configured its installation. If you do not have it yet, you can install it at the following link: https://www.postgresql.org/download/ 
Having configured this manager you must create the workshop2 database and within it the grammys table, to be able to insert the data into this table and then bring it. You do this process in one of the notebooks in the Notebooks folder.
Now, after you have opened docker, we proceed to run docker compouse, inside the airflow_first_dag folder is another readme with detailed information on what you should do.

If you want to make and see the edits that were made to each of the datasets, then go to the notebooks folder, each of these are Jupyter Notebooks, a way to run code by cells, and proceed to run each cell in order.

Now that you have all these parts done, it is time to run the dag. If you have already entered localhost:8080, you should see that many days appear and that the first one is called "dag_workshop". After this, enter this dag so you can see the graphs.
After this what you should do is run the dag, how do you do it? At the top left, not so high up, is a play button, click there and see how the airflow automation runs the project.

## Dashboard

To see the dashboar you must enter here: **([workshop2.pdf](https://github.com/JuancaBurbano/workshop2/files/15057543/workshop2.pdf))**.

## Reporte
To see the report that I have created about this project you can see it in the following link: https://docs.google.com/document/d/1NBlA778qiSLdZA64eNcdaWKpzHigMIywle_AJxlxTkw/edit?usp=sharing 
## Contacto

auto_awesome
Se muestra la traducción de Mi correo es el siguiente por si deseas hacerme una consulta:
Traducir Mi correo es el siguinete por si deseas hacerme una consulta:
61 / 5.000
Resultados de traducción
Resultado de traducción
My email is the following in case you want to ask me a question: camilitoburher17@gmail.com
