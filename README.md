# vagrant-minikube

```
vagrant up
vagrant ssh
```
## Cluster access
```
kubectl config set-cluster local --server=http://192.168.50.4:30000
kubectl config set-context local --cluster=local
kubectl config use-context local
```

## Docker registry
```
192.168.50.4:5000
```