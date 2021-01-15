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
 2. Initialize cluster networking
 3. kubeadm join - добавить оды в кластер

-------------
## Кастомизация 

Показать текущие ноды кластера
```bash
kubectl get nodes ```

поменять label для нейм node2
```bash
kubectl label  node node2 node-role.kubernetes.io/worker=
```

