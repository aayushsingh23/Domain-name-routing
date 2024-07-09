
# Domain-name Routing using Nginx

It generates three pods and deploys then using their respective services.

Nginx's HTTP Reverse proxy system helps to configure Domain-name routing such that all the three pods can be acessed with their respective domain names.



## Deploying Pods and its Services

Generating Pods

```bash
    kubectl apply -f pod.yaml
```

Starting services

```bash
    kubectl apply -f pod-service.yaml
```

## Configuring ConfigMap

To configure ConfigMap

```bash
    kubectl apply -f confMap.yaml
```
Deploying ConfMap

```bash
    kubectl apply -f deploy-conf.yaml
```
Service for ConfigMap
```bash
    kubectl apply -f deploy-service.yaml
```

## Testing our Deployment

Start Minikube Tunnel

```bash
    minikube tunnel
```

To test your deployed services go to the browser check if the pods are accesible through the provided domain names, in our case being:

```bash
    http://pod1.example.com
    http://pod2.example.com
    http://pod3.example.com
```
## Documentation

[Kubernetes](https://kubernetes.io/docs/home/)

[Minikube](https://minikube.sigs.k8s.io/docs/)

[Nginx](https://nginx.org/en/docs/)

