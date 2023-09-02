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
Kubernetes solves all the above problems.
