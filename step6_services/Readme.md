#Services 


## Service types :
 ### приложение доступно 
 * СlusterIP     - только по ip внутри k8s cluster. Только внутри 
 - NodePort      - Получaем определенный порт на всех Woker Nodes. Доступен на всех 
 - ExternalName  - DNS CNAME
 - LoadBalancer  - Только в cloud claser. LB создается автоматически и приаттачвается к подам 

## СlusterIP  Service type  
 create deployment 
```bash
  kubectl create deployment  evad-deployment  --image sevad/spring-h2-rest:v1.0.1
 ```
   
  scale deployment 
```bash
  kubectl scale deployment evad-deployment --replicas 3 
```

Create a Service object that exposes an external IP address.
```bash
kubectl expose deployment evad-deployment --type=ClusterIP --port 8000
```

Display information about your ReplicaSet objects:
```bash
    kubectl get svc
```

To verify the pods address 
```bash
    kubectl get pods --output=wide
```

-------------------------------------------
## Service type : NODEPORT
-------------------------------------------
 1. create deployment 
 2. create replicas
 3. expose service  
```bash
kubectl expose deployment/evad-deployment --type="NodePort" --port 8000
```

### View the Service
Берем отсюда NodePort
```bash
    kubectl get service evad-deployment --output yaml
```
берем отсюда INTERNAL-IP 
### The output shows the **_external IP addresses_** of your nodes:
```bash
kubectl get nodes --output wide
```

Access your Service
[node-ip-address]:[node-port]
 in my machine 
check app: 
```http request
http://192.168.49.2:30937/
```
----------------------------------------------------------------
## Load balancer Type 
-------------------------------------------
```bash
kubectl expose deployment/evad-deployment --type="LoadBalancer" --port 8000
```

check
```bash
kubectl get svc
```

--------------------------------------
манифесты 

In this case, there is no LoadBalancer integrated (unlike AWS or Google Cloud). With this default setup, you can only use NodePort or an Ingress Controller.
---------------

## How to user in minikube 
```bash
   minikube ip 
```

```
 kubectl patch svc my-multi-pods-service  -p '{"spec": {"type": "LoadBalancer", "externalIPs":["192.168.49.2"]}}'
```
```bash
  kubectl get svc
```