# Simple deployment for Kubernetes
Deployment manifest for nginx with a service type load balancer exposed on port TCP/80.
The purpose of this manifest is to test any Kubernetes cluster with the creation of a load balancer

To deploy the manifest, run the command:
```
kubectl apply -f https://raw.githubusercontent.com/oracle-devrel/oci-oke-virtual-nodes/main/nginx-svc/nginx.yaml
```
