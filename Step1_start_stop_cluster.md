# Create a Kubernetes cluster

Основной компонент **Cluster**. Мы создаем кластер который состоит из **Nodes**

* **Kubectl** для управления кластером. Основная компонента
* **Minikube** -для создания K8s Cluster single node
 

# Поднятие простого кластер
## Проверяем что все установлено

Показать версию minikube
```bash
   minikube version
```
Показать версию kubectl client'a и сервера
```bash
   kubectl version
```

## Запуск 

Cоздать и запустить K8s кластер с параметрами по умолчанию
```bash
   minikube start
```
затем будет создана и запущена виртуальная машина
Расположение конфигурации
------
~/[SYSTEM USER]/.kube/config
------

# Проверяем что сейчас на локальной ноде 

## состояние K8s кластера
```bash
   kubectl get componentstatuses
```

## Инфа по текущему кластеру 
```bash
  kubectl cluster-info
```

## Из каких серверов состоит кластер. Показать все серверы
``` bash
   kubectl get nodes
```

## Зайти на кластер 
```bash
   minikube ssh
```

## стопнуть и освободить память
```bash
   minikube stop
```
