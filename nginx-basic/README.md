# Nginx Deployment in Kubernetes

This guide will help you deploy an Nginx server in a Kubernetes cluster and serve a custom `index.html` file.

## Prerequisites

- A running Kubernetes cluster
- `kubectl` installed and configured to interact with your cluster

## How to run you 1st pod

1. Create a ConfigMap from the index.html file Run the following command to create a ConfigMap named nginx-index:

```bash
kubectl create configmap nginx-index --from-file=index.html
```

2. Apply the configuration with the following command:

```bash
kubectl apply -f nginx-deployment.yaml
```

3. Create a Service for the Nginx Deployment You can expose the Nginx deployment using a Service, which will provide network access to the Nginx pod.

```bash
kubectl apply -f nginx-service.yaml
```

4. Access the Nginx Site Once the Service is created, you can get the external IP address with the following command:

```bash
kubectl get service nginx-service
```


## Authors

* **Prashant Piprotar** - - [Prash+](https://github.com/prashplus)

For more Tech Stuff
### http://prashplus.blogspot.com