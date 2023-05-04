# Kubernetes Dashboard deployment on OKE Virtual Nodes
Deployment file for Kubernetes Dashboard on OKE Virtual Nodes.
This is a modified version from the upstream deployment file at https://github.com/kubernetes/dashboard.

## Change Log
The following lines are commented out from https://raw.githubusercontent.com/kubernetes/dashboard/v2.7.0/aio/deploy/recommended.yaml.
- 211 to 222
- 292 to 296

## Getting started
Deploy the dashboard in a cluster with virtual nodes using:
```
kubectl apply -f https://raw.githubusercontent.com/oracle-devrel/oci-oke-virtual-nodes/main/kubernetes-dashboard/recommended.yaml
```
Create an admin user:
```
kubectl apply -f https://raw.githubusercontent.com/oracle-devrel/oci-oke-virtual-nodes/main/kubernetes-dashboard/admin-user.yaml
```
Create a token and copy its value:
```
kubectl -n kubernetes-dashboard create token admin-user
```
Start a proxy on your workstation to access the dashboard:
```
kubectl proxy
```
Now access Dashboard at http://localhost:8001/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetes-dashboard:/proxy/
