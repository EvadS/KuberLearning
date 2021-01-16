# Игровая площадка PWK
можно создать 3 ноды согласно инструкциям в терминале 

```http
  https://labs.play-with-k8s.com
```
сессия на 4 часа 
максимум 5 нод в кластере 
--------------------------
##  запуск  
в каждом окне подсказки что делать. Последовательность. 


 1. Initializes cluster master node:
There will be command on bottom 
sample
 kubeadm init --apiserver-advertise-address $(hostname -i) --pod-network-cidr 10.5.0.0/16
---

 2. Initialize cluster networking
3-я пока не надо 

 3. kubeadm join - добавить оды в кластер

найти строку и запустить на нужной ноде 
Then you can join any number of worker nodes by running the following on each as root:

kubeadm join 192.168.0.13:6443 --token npp4dy.fz30vetwh97f36ss \
    --discovery-token-ca-cert-hash sha256:c9f775e2766c89f9a32bded48880a866b6cb8154b9000be6178ae8dde89ea9b7

-------------
## Кастомизация 

Показать текущие ноды кластера
```bash
kubectl get nodes ```

поменять label для нейм node2
```bash
kubectl label  node node2 node-role.kubernetes.io/worker=
```

