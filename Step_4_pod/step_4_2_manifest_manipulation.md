

Управление подами при помощи manifest файлов

запуск минимальной конфигурации 

```bash
kubectl apply -f manifests/pod-hello.yaml
```

для обновления - грохнуть
```bash
kubectl delete -f manifests/pod-hello.yaml
```

## Порт форвардинг 
```
kubectl port-forward hello 18000:8000
```

## few containers in pod 

pod-my-spring-ver2
2 контейнера:
  мой докер со спрингом 
  какой-то базовый томкат 

```bash
 kubectl apply -f manifests/pod-my-spring-ver2.yaml
```

порт форвардинг 

томкат
```bash
  kubectl port-forward my-spring-web-and-tomcat 5555:8080
```

спринг
```bash
  kubectl port-forward my-spring-web-and-tomcat 5555:8000
```





