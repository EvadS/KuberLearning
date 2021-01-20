
Base 

https://medium.com/@tech2020/hello-spring-boot-docker-kubernetes-on-windows-a1da30b40e8e

Create a Minikube deployment configuration
```bash
 kubectl apply -f demo.yaml
```

Expose Spring Boot
```bash
kubectl expose deployment/demo --type="NodePort" --port 8000
```

minikube ip
```
172.17.0.3:30802
```

write tcp 10.238.1.243:37034: write: no route to host




iptables --flush
iptables -tnat --flush
systemctl stop firewalld
systemctl disable firewalld
systemctl restart docker

