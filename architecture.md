**Architecture oF Kubernetes**
------------------------------

Kubernetes has a control plane and a **data plane**.

**Components of control plane**
-------------------------------
 - API Server
 - etcd
 - Scheduler
 - Controller Manager
 - Cloud Controller Manager(CCM)

**Components of data plane**
-----------------------------
 - Kubelet
 - Kubeproxy
 - Container Run Time

- In ***Docker*** simplest thing is - ***Container***
- In ***Kubernetes*** simplest thing is - ***Pod***
- For container to run, container should have a container run time. For ***Java application*** to run on Docker container, it should have a ***java run time***.
- In Docker there is a container run time environment called ***Docker Shim***.
- In production, there exist multiple master and multiple worker nodes.
- In Kubernetes, the request is not directly sent to worker, but through master nodes.
- The request always goes through control plane.
- ***Container pod is like a wrapper over the container which has some advanced capabilities***.

**KUBELET**
- Responsible for running/maintaining the pod on data plane(worker node).
- Responsible for running application.
- Keeps a check if pod is running or not.
- If not running, informs kubernetes component(api server), with auto healing feature kubernetes tries to correct that maybe by 
  restarting.

**KUBE PROXY**
- In docker there is Docker0 or default networking called bridge network.
- In Kubernetes, kube proxy provides networking. 
- It provides IP address to pod/container and load balancing capabilities.

**CONTAINER RUN TIME**
- Actually responsible for running container.






