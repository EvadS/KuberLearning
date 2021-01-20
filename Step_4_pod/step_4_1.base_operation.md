# Pod
Под — это абстрактный объект Kubernetes, представляющий собой группу из одного или нескольких контейнеров приложения (например, Docker или rkt) и совместно используемых ресурсов для этих контейнеров.

# шаг1
Поднимаем кластер
```bash
   minikube start
```
## Смотрим что есть 
```bash 
   kubectl get pods
```

## Создать под
```bash
   kubectl run test-pod-name --generator=run.pod/v1 --image=sevad/spring-h2-rest:v1.0.0 --port=8000
```

## просмотреть инфу 
```bash
   kubectl describe pod test-pod-name
```

## удалить под  
```bash
   kubectl delete pods test-pod-name
```

## зайти на под
выполнить комманду в контйнере
```bash
   kubectl exec test-pod-name date
```

## запустить комманду и остаться в интерактивной режиме
```bash
   kubectl exec -it  test-pod-name  sh
```

## Логи
```bash
   kubectl logs test-pod-name 
```

## Порт форвардинг, доступ к тому что в Pods из вне 
Обычно делается через сервис

```
kubectl port-forward test-pod-name 18000:8000

```
8000 - внутненний 
7788 - внешний

test

kubectl port-forward demo-54d568dc4f-ns7vz 18000:8000











