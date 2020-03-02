# STEFAN MICHEL - Udagram Kubernetes Project 

## How to setup the project:

enter your secrets and configs in the udacity-c3-deployment/k8s/ config files: aws-secret.yaml, env-configmap.yaml, env-secret.yaml

run: 

```
cd udacity-c3-deployment/k8s/

kubectl apply -f aws-secret.yaml
kubectl apply -f env-configmap.yaml
kubectl apply -f env-secret.yaml

kubectl apply -f backend-feed-service.yaml
kubectl apply -f backend-user-service.yaml
kubectl apply -f frontend-service.yaml
kubectl apply -f reverseproxy-service.yaml

kubectl apply -f backend-feed-deployment.yaml
kubectl apply -f backend-user-deployment.yaml
kubectl apply -f frontend-deployment.yaml
kubectl apply -f reverseproxy-deployment.yaml

kubectl port-forward svc/reverseproxy 8080:8080
kubectl port-forward svc/frontend 8100:8100
```

