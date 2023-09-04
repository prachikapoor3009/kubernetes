**Why deployment?**
-------------------
- It is unlikely that pod is deployed directly in Kubernetes.
- As pod is more likely like a docker container.
- Deployment ensures auto scaling and auto healing which pod/container doesn't.
- Deployment will ensure no downtime of application running inside the application.
- Deployment uses some strategy called **rolling update strategy/recreate strategy**.
- Ensures number of **replica sets** mentioned in deployment file matches with number of pods always available on kubernetes cluster.
- Suppose replica sets mentioned in deployment file is mentioned to be 2, meaning 2 copies of application should always be  
  running on the kubernetes cluster, so replica set which is a kubernetes controller maintains the state of pods.

**Image**
----------
![image](https://github.com/prachikapoor3009/kubernetes/assets/66333390/c9abc4d8-5a32-4f7b-a103-dd62ee2e3262)

**Replica Sets**
-----------------
- Alternative/upgrade version of replication controller.
- Gurantees the availability of specified number of identical pods.
- Specifies selectors, replicas and a pod template.

**Sample Deployment**
---------------------
apiVersion: apps/v1
kind:Deployment
metadata:
  name: example-deployment
  labels:
    role: example
spec:
replicas: 4
  selector:
    matchLabels:
      role: example
  template: 
    metadata: 
      labels: 
        role:example
    spec:
      containers:
      - name: nginx
        image: nginx
        ports:
        - containerPort: 80
    



