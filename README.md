# CUmulus_tutorials
Tutorials and example workflows for CURC's on-prem cloud

## Login
- CUmulus portal
- Check we have prereqs for course (CUmlulus access, twitter dev account)

## Instance Creation
- Walk through instance creation
- Walk through ssh key

## Instance Management/Admin
- Log into instance
- Admin?

## Create project
- environment file

## Docker
- brief discussion on containers
- install docker (easy script)
- test installs (version or docker hello world)

## Docker-Compose
- brief discussion about docker-compose
- install docker-compose (easy script)
- test install (version)

### Database
- we'll use the mysql db container

### phpMyAdmin (Web based interface to manage db)
- we'll use the phpMyAdmin web interfact to manage our db

## Persistant storage (necessary in this course?)

## Twitter API
- twitter dev accounts
the username of the person who wrote the tweet, the time it was created, the tweet, the retweet count, the place the tweet originated and the location (more on these below). This corresponds to 6 columns plus the primary key and we can define the datatypes as follows:

    primary key: INT(11)
    username: VARCHAR(255)
    created_at: VARCHAR(45)
    tweet: TEXT
    retweet_count: INT(11)
    location: VARCHAR(100)
    place: VARCHAR(100)

## Python
- create a class that allows us to connect to the Twitter API.
- create some code that connects to our database and reads the data into the correct columns.


