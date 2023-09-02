# Kubernetes
A container orchestration tool.
Containers are ephemeral in nature(short lived in nature).
Containers can die and revive anytime.
**Reasons can be:**
- Lack of memory resources
- Image not getting pulled
Processes are killed based on some priority set by Kernel.
Suppose container 1 was taking a lot of resources due to which container 100, wasn't even coming up.
So, one container impacts the other container. The applicaton running inside other container will not be accessible.

**Docker Drawbacks**
---------------------
- **Single host nature of Docker container** - One single host, docker is installed and then containers are created on top of it.
- **Auto healing** - Without user's manual intervention, container should start by itself. But it doesn't happen in Docker.
- **Auto scaling** - Increasing number of containers as per traffic by itself.(Load balancing at back end).
- **Minimalistic/Simple platform** - Does not support enterprise level support.(Standards - Enterprise application should have 
   Load Balancer, Firewall, Autoscale, Autoheal, API gateways).

**Solution**
-------------
Kubernetes

**How Kubernetes solves all problems?**
----------------------------------------
- By default, Kubernetes is a **cluster**.
- Cluster is a collection/group of **nodes**.
- Kubernetes is installed in a **master slave** architecture.
- Multiple node architecture . example - 1 master node , n slave nodes.
- If one node is faulty(container inside it), it shouldn't impact the other container. That container is put by kubernetes inside 
  other node.
- For auto helaing, kubernetes has **Replica sets**. No need to deploy a new container on increased load, in yaml file of replica 
  set, set replicas to be increased to say 10.
- **Horizontal pod autoscaler** : Increased load, increase number of containers. Threshold of container reached, automatically 
  spin up a container.


