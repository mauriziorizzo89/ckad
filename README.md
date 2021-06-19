# Local Kuberentes cluster configurazion with 3 worker nodes

```` 
 minikube start --nodes 3 -p mr-cluster
 ```` 
 
 or 
 
 ```` 
 minikube start --driver=docker --nodes 3 -p mr-cluster
```` 

# Label worker nodes

```` 
kubectl label node <node-name> node-role.kubernetes.io/worker=worker
````  
 
````  
kubectl get nodes                                                      
NAME             STATUS   ROLES                  AGE     VERSION
mr-cluster       Ready    control-plane,master   9m23s   v1.20.7
mr-cluster-m02   Ready    worker                 6m30s   v1.20.7
mr-cluster-m03   Ready    worker                 4m7s    v1.20.7
```` 
