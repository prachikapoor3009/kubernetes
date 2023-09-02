**What is pod?**
- Smallest deployable units of computing which can be created and managed in Kubernetes.
- Group of one or more containers, with shared storage and network resources.
- Defines how a container can run.
- Below image shows pod containing two containers but share same networking namespace meaning, both containers can communicate 
  with each other.
- In Kubernetes, containers can not be created directly.

**Image**
![image](https://github.com/prachikapoor3009/kubernetes/assets/66333390/b39f9539-5f7a-4fbb-baa8-1f17c4bc5a7d)

**Pod definition - yaml - manifests/resources**
-----------------------------------------------
**pod.yml**
apiVersion: v1
kind: Pod
metadata: 
    name: nginx
spec:
    containers:
    - name: nginx
      image: nginx:1.14.2
      ports:
      - containerPort: 80

**Command to create pod**
 - ***kubectl create -f pod.yml***
 - Kubernetes send this request to API server and created a pod.
 - pod/nginx created.
 - Verify by:
   ***kubectl get pods***
   ***kubectl get pods -o wide*** -> will also IP address of the pod.
 - Check if application is running:
   ***minikube ssh -p <cluster_name>***
   ***curl <IP of pod>***
.

