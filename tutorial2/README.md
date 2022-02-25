# Establish a MySQL database to query Twitter and store results

___Learning Objective:___

We will use CUmulus to create an instance with a persistent database (MySQL) and a python application which will use the Twitter API and a Flask web server to query data from Twitter and store it in the database. The following uses docker containers to allow simple build-up/tear-down of the applications (a full discussion of Docker is out of the scope of this tutorial). This tutorial showcases a few important features of Cumulus:
* A persistent workflow not limited by wall clock times (such as on HPC systems)
* User administration of compute resources (using root privileges for applications such as Docker) 
* Routable floating IPs that enable you to access your instance via the Internet.
