# ingress-nginx deployment on OKE Virtual Nodes
Deployment file for ingress-nginx on OKE Virtual Nodes.
This is a modified version from the upstream deployment file at https://github.com/kubernetes/ingress-nginx of ingress-nginx version 1.9.3.

Deploy Nginx Ingress Controller in a cluster with virtual nodes using:
```
kubectl apply -f https://raw.githubusercontent.com/oracle-devrel/oci-oke-virtual-nodes/main/ingress-nginx/deploy.yaml
```

## Change Log
The following lines are commented out from the ingress-nginx deployment manifest version 1.9.3: https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/static/provider/cloud/deploy.yaml.
- lines 488 to 493
```
          allowPrivilegeEscalation: true
          capabilities:
            add:
            - NET_BIND_SERVICE
            drop:
            - ALL
```
- lines 551 and 600
```
        fsGroup: 2000
```

Previously, the following lines are commented out from the ingress-nginx deployment manifest version 1.7.0: https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/static/provider/cloud/deploy.yaml.
- lines 484 to 490
- line 542
- lines 547 to 549
- line 591
- lines 596 to 598
