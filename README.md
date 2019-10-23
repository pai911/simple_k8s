# simple_k8s
- A simple k8s configuration that uses Pod and Service/NodePort
- Single container/pod 

## Initial Config
This demonstrate that only a limited set of fields can be updated in a Pod config
### Pod
A pod with an image from Docker Hub
- client-pod.yaml

### Service/NodePort
A NodePort service that config the external port for local computer 
- client-node-port.yaml

You can expect to see the following error message if you change the containerPort in the Pod config file.

> The Pod "client-pod" is invalid: spec: Forbidden: pod updates may not change fields other than `spec.containers[*].image`, `spec.initContainers[*].image`, `spec.activeDeadlineSeconds` or `spec.tolerations` (only additions to existing tolerations)

## Production Config
We then use deployment to provides declarative updates for Pods
### Deployment
A deployment to run a set of identical pods (with an image from Docker Hub)
- client-deployment.yaml
