# Creating a CUmulus instance

---

#### _Learning Objectives:_

* Logging into CUmulus via Horizon (the CUmulus web portal)
* Creating your instance (i.e. virtual machine)
* Logging into your instance via `ssh` 

---
###  Part 1: Logging in to CUmulus via Horizon
---

_Horizon is the CUmulus web portal, hosted at https://cumulus.rc.colorado.edu. Let’s take a brief tour of Horizon_

#### _Log in with your institution’s credentials:_

Navigate to https://cumulus.rc.colorado.edu and authenticate using your insitution's credentials (e.g., University of Colorado Boulder)

<p align="center">
<img src="images/login.png" width="40%" />
</p>

---

#### _Navigate Horizon_

* Choose your project (top left)
  * Generally users only have 1 project

* There are 4 main sections
  * `Compute`
  * `Volumes`
  * `Networks`
  * `Orchestration`
 
<p align="left">
<img src="images/navigate_intro.png" width="35%" />
</p>

---

#### _Navigate Horizon: Overview_

* Land on the Overview page under “Compute” to get a quick summary of your project

<p align="center">
<img src="images/navigate_overview.png" width="70%" />
</p>

---

#### _Navigate Horizon: Instances_

* Navigate to: `Project->Compute->Instances`

* An Instance is just a digital version of a physical computer.
  * Instances can perform almost all of the same functions as a computer, including running applications and operating systems.

* You are now ready for instance creation! ...


---
### Part 2: Instance Creation
---

* From here, let’s create a simple instance
  * From the Instances page click “_Launch Instance_” to begin creating your virtual machine.

#### _Instance creation: Details_
 
The first instance creation screen is entiled ___Details___: 

<p align="center">
<img src="images/instance_details.png" width="70%" />
</p>

* Fill out the instance _name_ and _description_
  * _availability zone_ and _count_ can be left as defaults
  * click `Next` when done to go to the ___Source___ screen.
 
---

#### _Instance creation: Source_

You can choose an operating system from the images CURC provides

Choose to have your storage volume deleted on Instance Deletion
If you select fno” be aware of “zombie” volumes that will stay around when the instance is deleted
15

Flavor
Choose from a list of pre-selected resources:
“Flavors” manage the sizing for the compute, memory, and storage of the instance.
16

Networks & Network Ports
Select a project network, which determines routability of either a public/internet or campus/internal floating IP.
We’ll choose an external network

Ports provide extra communication channels to your instances. 

You can select ports instead of networks or a mix of both.
17

Security Groups
Security Groups act as a virtual firewall for your instance to control inbound and outbound traffic.

We’ll pick ssh-restricted, http, and https for our demo
18

Key Pair
A key pair allows you to SSH into your new instance.

You may select an existing key pair, import a key pair, or generate a new key pair.

I find it easiest to create a keypair on my local machine and import it
https://www.ssh.com/academy/ssh/public-key-authentication 
19

Config, Server Group, Scheduler Hints, and Metadata
We’ll leave these as defaults as they are extra configuration we can provide our instances, but not necessary 
20

Launch Instance and Associate IP
Launch instance and wait for it to be set up

We can then associate a Floating IP which will allow us to access the instance from outside of the CU network
On the right hand side of the newly created instance choose “Associate Floating IP” under the “actions” dropdown
21

Associate IP
Select from available IP addresses
If needed you can add a floating IP, but be aware there are limited numbers of floating IPs

Select port to be associated
This should be pre-populated with the internal IP of your new instance
22

Logging into your Instance
23

Logging In
You must be on CU VPN to connect via ssh (CURC restriction)

Open up an ssh connection providing the identity (key) file:
$ ssh -i ~/.ssh/<private key> <hostname>@<external floating IP>

For an ubuntu instance this may look something like:
$ ssh -i ~/.ssh/testkey ubuntu@123.456.789.123
24

Logged In
Congratulations! You are now logged into your instance

You can now:
Install Software
Administer your instance
Run applications and jobs
  
## Additional Information
  * [CUmulus documentation](https://curc.readthedocs.io/en/latest/hybrid-cloud/cumulus.html)
