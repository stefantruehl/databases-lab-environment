# Database Lab Environment

This is a very simple, quick, dirty, and ugly project that is supposed to help students to spin up a local database environment. This environnement can, for example be used to complete (most) lab exercises of my database lectures.

In fact, it is simply a [Docker Compose file](https://docs.docker.com/compose/) (plus some dockerfile) that allows you to quickly spin up containers on your local machine.  

The environment consists of:
1. **PostgreSQL**: database server ([link-1](https://en.wikipedia.org/wiki/PostgreSQL), [link-2](https://www.postgresql.org/)).
2. **pgAdmin4** as web-based database client for PostgreSQL. It has a very nice and powerful UI ([link](https://www.pgadmin.org/)). As part of this project, it already is prefigured to access the database above. 

If you are familiar with the usage of Docker Compose you will not need this, but if you are not, find some explainations on how to use this project below. 
 

## How to use this Project?!
### Precondition
1. Make sure you have a working version of Docker on your machine. Installation guide can be found [here](https://docs.docker.com/install/).
2. Make sure you have a working version of Docker Compose installed. Installation guide can be found [here](https://docs.docker.com/compose/install/).
3. Clone/Download this repository on your local machine. If necessary, get yourself familiar with Git [here](https://git-scm.com/).

In order to use the environment, execute the following commands in the local folder where you cloned the repository. Please, acknowledge in most cases, all commands must be executed with root privileges. 

### Start the Environment
````
docker-compose up
````
Will start the environment. The first time (or after you removed them from your system) the containers will be created, downloaded to your system and started. 
Once the containers have started, you find the pgAdmin4 interface at [http://localhost:5050](http://localhost:5050). Use the following credentials to login:
- **User:** user
- **Password:** secretpassword

In pgAdmin you will already see your local PostgreSQL database ready to be used. 


### Stop the Environment
````
docker-compose stop
````
Stops the containers for future use or removal.


### Remove stopped Containers from your Machine
````
docker-compose rm
````
Once the containers are stopped, you can deleted them from your system. 


## Connect another Application to the Database
If you want to connect another application to the database, you need to connect to:
- **Server:** localhost:5432
- **Database:** dbadmin; new databases can of cause be created
- **User:** dbadmin
- **Password:** dbadminpassword

## Preconfigured User Credentials

The following are the standard credentials that are hard coded into the deployment process. You may want to create additional credential once you use the environment 

For the **database** the standard credentials are: 
- **User:** dbadmin
- **Password:** dbadminpassword

For the **pgAdmin** the standard credentials are: 
- **User:** user
- **Password:** secretpassword

Please note: all above credentials are hard-coded into the deployment process. Thus, please don't change them (and, yes I know this is ugly).

## Disclaimer
This project is in a quick-and-dirty state. Hard-coded credentials are ugly, bad, and evil. However, I have not found a quick way of registering a database in a dynamic way. I may continue this in the future. 
