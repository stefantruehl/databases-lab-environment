Database Lab Environment

In this repository you find a compose file that allows you to quickly spin up a PostgreSQL container and 
 

# How to use it
Precondition: make sure you have a working version of docker-compose [installed](https://docs.docker.com/compose/install/).



# Preconfigured User Credentials

The following are the standard credentials that are hardcoded into the deployment process. You may want to create additional credential once you use the environment 

For the **database** the standard credentials are: 
- **User:** dbadmin
- **Password:** dbadminpassword

For the **pgAdmin** the standard credentials are: 
- **User:** user
- **Password:** secretpassword

Please note: all above credentials are hardcoded into the deployment process. Thus, please don't change them (and, yes I know this is ugly).

# Disclaimer
This project is in a quick-and-dirty state. It works for me at the moment
