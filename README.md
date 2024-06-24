# Objectives:
* To create a Mutli-tier web application stack
* Pre-requisite setup for upcoming tasks
* Setup real world projects on local machine automatically

## Problems: 
* Setup on Laptop/Desktop locally 
  - avoid making commits to a server due to insecurity
  - avoid commiting to a local stack due to
      - unrepeatability (if done manually)
      - time consumption
      - complexity (setting up a local server using VMs is complex)

Such a scenario creates problems.

## Solution:

The Local Setup is automated, made repeatable with the use of Infrastructure as a Code (IaaC).

## Tools:
* Hypervisor - Oracle VM VirtualBox
* Automation - Vagrant
* CLI - GitBash
* IDE - Visual Studio


Architectural Design for various services in our stack:
![architecture for vProfile](https://github.com/aneeshahehe/vProfile-project-setup-Local-/assets/104615902/e8298bfa-e732-4ff8-988a-5cb3f4242988)

The word 'stack' is used for collection of servicesworking together to create an experience.
## Services to be deployed
* MySQL/MariaDB - SQL Database
* Memcache - DB Caching
* RabbitMQ - Broker/Queuing Agent
* Tomcat - Application Server
* Nginx - Web Service

Workflow and configurations of architecture :
* The user enters an IP address (not a URL) on a web browser.
* This leads to a Load Balancer.
* Nginx : It's  web service which is used to create a load balancing experience. Upon receiving the request, it routes the request to Tomcat server.
* Tomcat : It's a Java web application service which is used to host web applications written in Java by developers.
* NFS : Shared external storage
* MySQL DB : Login details of the user are stored here.
* Rabbit MQ : Message broker or also called a Queuing agent to connect to applications together.
* Mem cache : A database caching service, connected with MySQL server.
  
  



