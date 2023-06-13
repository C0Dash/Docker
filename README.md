# Docker Networking
Docker Networking enables user to link a Docker container to as many as networks as he/she requires.
Docker Networking is used to provide complete isolation for Docker continers.

There are five types of Network drivers available -
1. bridge - Its private default network creates on the host. Container with in this network will have private IP through which they can communicate with each other. The docker server(daemon) creates virtual ethernet bridge docker0 that performs the operation by automatically delivering packets among various network interfaces.
2. Host - Its a public network. Use Host IP and TCP port in order to display services running inside container. It disables the isolation between docker host and dokcer container which means using this network driver a user will be unable to run multiple containers on the same host. 
3. None - In this network driver, the docker container will neither have any access to external networks nor will it be able to communicate with other containers. This option is to disbale total network funcationality.  
4. Overlay - Creating internal private network to docker nodes in the docker swarm cluster. In swarm orchistration, there are master node, worker nodes etc which required overlay network.
5. MacVlan - Simplifies the communication b/w containers. This network assigns a MAC Address to the container. With MAC address the Docker server(Daemon) routes the network traffic to a router. Its suitable when user want to directly connect the continer to a physical network rather than docker host. 
Commands -
Docker network list - lists the network drivers available
Docker network inspect bridge - to display the network
Docker attach container - to connect to a container
ip address show


# Docker Swarm?
Docker Swarm is a service which allows users to create and manage a cluster of docker nodes and schedule containers
Each node in the docker swarm is a Docker Daemon and all Docker Daemon interact using the Docker API. 

Features of Docker Swarm -
Decentralized Access
High Security
Auto Load Balancing
High Scalabilty
Roll-back task

Two types of nodes -
- Manager Node - Maintains cluster management tasks. API, Orchestration, Task Allocation, Dispatcher and Scheduler
- Worker Node - Executes the instruction that manager nodes provides. Checks the task, executes the tasks


