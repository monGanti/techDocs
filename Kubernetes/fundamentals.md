# Kubernetes 

## Container + orchestration

#### Problem overview
when you have to setup a dev or production environment where we use the following for example: 
* Node for web server
* mongo DB for Database
* any Messaging service
* ansible for orchestration 
they all might have different libraries/ dependencies / OS requirement / hardware infrastructure requirements etc. Always checking for their compatabilites/ dependencies + extra long setup time + unsure if the full setup with work on different Dev/QA/Prod environments is a night-mare. 

If they independently stayed on a seperate containers along with their respective libraries and dependencies on the same OS kernel and hardware infrastructure then almost 80% of the deployment consistencies can be achieved. 

#### What are Containers
Containers are completely isolated environments which has its own processes, network,mounts just like any VM except that they all share the same OS Kernel which stays beneath them. 

Containerization is NOT a new technology , it always existed but something like Docker utilizes an existing lxc format and provides very high level powerful functions which can send commands to these existing formats and that's what makes it a nice end-user friendly tool.

**Note:**  for an underlying Linux OS kernel , a windows container will not work as it will need a Windows OS kernel but any other softwares with linux compatablity will work. This is not a disadvantage as the main purpose of Docker is to give the ability to containarize the applications and not the complete VM capabilities. 

Also, VM's use more utilization and space which is typically not a dev need when it comes to simple applications seperation. 

*Image*
An image is an template of the package which you can use to recreate the containers. 

#### Advantages of Kubernetes 
Kubernetes has many more advantages compared to its competitors like docker swarn / mesos
1. Its an orchestration layer that will ensure high availability of applications as it resets any damaged nodes and rebuilds and keeps as many nodes as required wrt traffic
2. seemlessly spins up new applications and nodes 
3. maintains traffic with load balancer
4. you can do all of these with just few declarative object files 

*Kubernetes* is a container orchestration technology that can orcestrate and manage 100s or 1000s of containers in a clustered environment.

## Pods
Pods are like container clusters and always has 1-1 mapping with the containers. Usually 1 container exists per Pod. You can have more than 1 pods / node depending upon the space of the node. 

we are not restricted to maintainer 1 container/Pod. sometimes it takes helpers for the applications to run and we want to deploy those helpers in seperate containers and also want to maintain 1-1mapping of application container with the helper container. In such rare cases you cna have both those containers with in the same Pod. Main benefit of doing that is application and it's helper containers will share the same network (localhost) and storage space. 

refer to [Commands](commands.md)