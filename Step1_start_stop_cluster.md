# Create a Kubernetes cluster

Основной компонент **Cluster**. Мы создаем кластер который состоит из **Nodes**

* **Kubectl** для управления кластером. Основная компонента
* **Minikube** -для создания K8s Cluster single node
 

# Поднятие простого кластер
## Проверяем что все установлено

```bash
   minikube version
```

```bash
   kubectl version
```

## Запуск 

```bash
   minikube start
```
затем будет создана и запущена виртуальная машина
Расположение конфигурации
------
~/[SYSTEM USER]/.kube/config
------

## Проверяем что сейчас на локальной ноде 

### что сейчас с кластером 
Инфа по компонентам
```bash
   kubectl get componentstatuses
```

Инфа по текущему кластеру 
```bash
  kubectl cluster-info
```

Из каких серверов состоит кластер 
``` bash
   kubectl get nodes
```

Зайти на кластер 
```bash
	minikube ssh
```

стопнуть и освободить память
```bash
   minikube stop
```
