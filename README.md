# simple_k8s
A simple k8s configuration that uses Pod and Service/NodePort

## Initial Config
This demonstrate that only a limited set of fields can be updated in a Pod config
### Pod
A pod with an image from Docker Hub
- client-pod.yaml

### Service/NodePort
A NodePort service that config the external port for local computer 
- client-node-port.yaml

## Production Config
We then use deployment to provides declarative updates for Pods
### Deployment
A deployment to run a set of identical pods (with an image from Docker Hub)
- client-deployment.yaml
