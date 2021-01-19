Deployments

Развёртывания Kubernetes
Как только вы запустили кластер Kubernetes, вы можете развернуть свои контейнеризированные приложения в него. Для этого вам нужно создать конфигурацию развёртывания (Deployment) в Kubernetes. Развёртывание сообщает Kubernetes, как создавать и обновлять экземпляры вашего приложения. После создания развёртывания ведущий узел Kubernetes планирует запустить экземпляры приложения на отдельных узлах в кластере.

```bash 
 minikube start
```

### создаем
```bash
kubectl create deployment evad-deployment --image sevad/spring-h2-rest:v1.0.0
```
depoyment создаст Pod

### смотрим 
```bash
kubectl get deploy
```

```bash
kubectl describe deployment evad-deployment
```

## Scaling 
```bash
kubectl scale deployment evad-deployment  --replicas 4 
```
в результате будет создана реплика 
```bash
    kubectl get rs
```
---
## удалить 
```bash
  kubectl delete deploy my-web-deployment
``
--
```bash 
kubectl apply -f https://raw.githubusercontent.com/EvadS/KuberLearning/main/Step_5_deployments/deployment-1-simple.yaml
```

--
```bash
 kubectl apply -f https://raw.githubusercontent.com/EvadS/KuberLearning/main/Step_5_deployments/deployment-2-replicas.yaml

```

смотрим 
```
kubectl get pods
```

```bash
kubectl port-forward my-web-deployment-replicas-56887b7cc7-rm5kd  18000:8000
```

3 реплики 

--

yaml's 

