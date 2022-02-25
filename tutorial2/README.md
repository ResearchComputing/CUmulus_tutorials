# Establish a MySQL database 

#### Twitter API

The first demo we'll take a look at is using Cumulus to create an instance with a persistent database (MySQL) and a python application which will use the Twitter API and a Flask web server to query data from Twitter and store it in the database. The following is with docker containers to allow simple build-up/tear-down of the applications (a full discussion of Docker is out of the scope of this demo). This demo showcases a few important features of Cumulus:
- A persistent workflow not limited by wall clock times (such as on HPC systems)
- User administration of compute resources (using root privileges for applications such as Docker) 
- Rout able floating IPs available on the internet.
