# vagrant-minikube

```
vagrant up
vagrant ssh
```
## Cluster access
```
kubectl config set-cluster local --server=http://localhost:30000
kubectl config set-context local --cluster=local
kubectl config use-context local
```