# Clearing the Fog: An introduction to CUmulus

CUmulus is CU Research Computing's free-to-use on-premise cloud service, which supports cases not well-suited for HPC such as webservers, databases, and long-running services.

The CUmulus service includes access to a Virtual Private Cloud (VPC) which provides users with a logically isolated section of the cloud with a small number of outside routable floating IP addresses. Within this VPC customers will be given an allocation of:

- CPU cores
- Memory
- Storage

## Today we're going to go cover: 
1) CUmulus Access 
	- Getting access to CUmulus and the allocation process
	- Logging into Horizon (CUmulus web portal)
	- Creation of an instance (i.e. virtual machine) within the a demo VPC
	- Logging into your instance via ssh   
2) Demo a workflow one might use CUmulus for: 
	- Query Twitter via the Twitter API and store data into a mySql database (using docker containers).

### CUmulus Access:

#### CUmulus Access and the Allocation Process
The application process for CUmulus requires users to submit an proposal for your use case, which can be requested by emailing rc-help@colorado.edu. In this proposal you will:

-  Describe your CUmulus workflow
-  Describe why your workflow is appropriate for CUmulus (over other CURC HPC resources). 
-  Estimate the resources you require (operating system, CPU cores, disk space, memory)

We will review your allocation and get back to you. This is an iterative process where we work with you to make sure the request for resources fits your (and our) needs. 

#### Login into Horizon 
- Check we have prereqs for course (CUmlulus access).

First we'll take a brief tour of Horizon, the Graphical Web Applicaiton that allows us to log into and administer our projects, first go to cumulus.rc.colorado.edu/.

#### Instance Creation
Instance creation can be confusing, but all we're doing here is creating a virtual machine that we can then log into and adminiter ourselves. We're going to go through instance creation step-by-step.

Let's step through creating our own instances.

A note on ssh keys: #todo 

#### Log into Instance 
- Log into instance
- Admin #todo, touch briefly on

### Demo Workflow(s):

#### Twitter API

The first demo we'll take a look at is using CUmulus to create an instance with a persistant database (mysql) and a python application which will use the Twitter API and a Flask webserver to query data from Twitter and store it in the database. The following is with docker containers to allow simple build-up/tear-down of the applications (a full discussion of Docker is out of the scope of this demo). This demo showcases a few important features of CUmulus:
- A persistant workflow not limted by wall clock times (such as on HPC systems)
- User administration of compute resources (using root privilages for applications such as Docker) 
- Routable floating IPs available on the internet

