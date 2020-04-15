# kubetest
A simple project for setting up a kubernetes development environment
# how to use
***
```
sudo snap alias microk8s.docker docker
sudo snap alias microk8s.kubectl kubectl
```
```
microk8s.enable registry
docker build -t localhost:32000/kubetest:v1.0.0 .
docker push localhost:32000/kubetest:v1.0.0
kubectl apply -f kubetest.yaml

```
然后
```
kubectl get pods
kubectl get svc
curl -i localhost:31065
curl -i localhost:30788/healthz
kubectl logs svc/kubetest

```
