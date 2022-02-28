
# Establish a MySQL database to query Twitter and Store Results

___Learning Objective:___

We will use CUmulus to create an instance with a persistent database (MySQL) and a python application which will use the Twitter API and a Flask web server to query data from Twitter and store it in the database. The following tutorial uses containers to allow simple build/tear-down and development of the application. 

> Note: An in depth discussion of Docker and Docker-Compose is out of the scope of this demo, but further reading will be provided when necessary.

This tutorial showcases a few important features of Cumulus:
* A persistent workflow not limited by wall clock times
* User administration of compute resources (using root privileges for applications such as Docker) 
* Routable floating IPs that enable you to access your instance via the Public Internet

## Tutorial

### Setup
Before we can get this application up and running in a CUmulus instance we have some house-keeping to take care of:
1) We need a working CUmulus instance with http port exposed (default 80) and a public floating IP. To add an http port to an instance you can do so within the instance creation launcher or after the instance has been created; add a floating IP after the instance has been created. For instructions on both see [tutorial 1].
2) In order to query Twitter with the Twitter API V2 you must first obtain a Twitter Developer Account and get access to a number of secret keys:
	-   go to the following website [https://developer.twitter.com/](https://developer.twitter.com/content/developer-twitter/en.html) and create an account.
	-   Once you have verified your email you can log into your account. You should be able to create a new app on the following webpage: [https://developer.twitter.com/en/apps](https://developer.twitter.com/en/apps)
	-   Fill in all the details about your app and then create your access token.
	-   Make a note of your consumer key, consumer secret, OAuth access token and OAuth access token secret. These are needed to connect to the API.
3) You will need to clone THIS github repo (which you have likely already done if following [tutorial1]). The code for this application lives in this git repo.
	- `cd` into into `/path/to/CUmulus_tutorial/tutorial2/app` directory
4) Once you have your Twitter API keys, we can set up our config file which will allow for our applications to grab the necessary passwords, ports, keys, etc. as environment variables.
	- Using a text editor of your choice create the file `/path/to/CUmulus_tutorial/tutorial2/app/.env` (*note the period in front of `.env`*) and paste the following lines in adding your web port (default 80 for http in CUmulus), your mysql password (you choose this), and your Twitter API keys. You can use the examples to format your environment variables.
```
#### Comment out or delete any unused entries

#### EXAMPLE 
# DO NOT USE QUOTES TO ENCLOSE THE VALUES
EXAMPLE_VARIABLE=true
EXAMPLE_PORT=1234
EXAMPLE_PASSWORD=kdos9lsk@1l1!
EXAMPLE_EMAIL=myemail@domain.com
EXAMPLE_IP=123.123.123.123

#### BELOW ARE SOME OF THE VARIABLES USED IN docker-compose.yml


WEB_PORT=

MYSQL_ROOT_PASSWORD=

API_KEY=
API_KEY_SECRET=
BEARER_TOKEN=
ACCESS_TOKEN=
ACCESS_TOKEN_SECRET=

```

### Docker
- install docker
  - test docker
- install docker-compose
  - test docker-compose
- review docker compose file

### Docker images
- python twitter web app
- mysql database

### Persistant Data
- docker volumes

