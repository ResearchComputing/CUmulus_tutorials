# Clearing the Fog! Getting Started on Cumulus, a Near to the Ground On Campus Cloud Solution

Cumulus is CU Research Computing's free-to-use on-premise cloud service, which supports cases not well-suited for HPC such as web servers, databases, and long-running services.

The Cumulus service includes access to a Virtual Private Cloud (VPC) which provides users with a logically isolated section of the cloud with a small number of outside rout able floating IP addresses. Within this VPC customers will be given an allocation of:

- CPU cores
- Memory
- Storage

## Today we're going to go cover: 
1) Cumulus Access 
	- Getting access to Cumulus and the allocation process
	- Logging into Horizon (Cumulus web portal)
	- Creation of an instance (i.e. virtual machine) within a demo VPC
	- Logging into your instance via ssh 
2) Demo a workflow one might use Cumulus for: 
	- Query Twitter via the Twitter API and store data into a MySQL database (using docker containers).

### Cumulus Access:

#### Cumulus Access and the Allocation Process
The application process for Cumulus requires users to submit a proposal for your use case, which can be requested by emailing rc-help@colorado.edu. In this proposal you will:

- Describe your Cumulus workflow
- Describe why your workflow is appropriate for Cumulus (over other CURC HPC resources). 
- Estimate the resources you require (operating system, CPU cores, disk space, memory)

We will review your allocation and get back to you. This is an iterative process where we work with you to make sure the request for resources fits your (and our) needs. 

### CUmulus Instance Creation and Log In

You can follow instance creation process and log in in the slides within this root directory as well as the CURC CUmulus documentation (https://curc.readthedocs.io/en/latest/hybrid-cloud/cumulus.html)

### Demo Workflow(s):

#### Twitter API

The first demo we'll take a look at is using Cumulus to create an instance with a persistent database (MySQL) and a python application which will use the Twitter API and a Flask web server to query data from Twitter and store it in the database. The following is with docker containers to allow simple build-up/tear-down of the applications (a full discussion of Docker is out of the scope of this demo). This demo showcases a few important features of Cumulus:
- A persistent workflow not limited by wall clock times (such as on HPC systems)
- User administration of compute resources (using root privileges for applications such as Docker) 
- Rout able floating IPs available on the internet.
