# metrics-server deployment on OKE Virtual Nodes
Deployment file for metrics-server on OKE Virtual Nodes.
This is a modified version from the upstream deployment file at https://github.com/kubernetes-sigs/metrics-server.

Deploy metrics server in a cluster with virtual nodes using:
```
kubectl apply -f https://raw.githubusercontent.com/oracle-devrel/oci-oke-virtual-nodes/main/metrics-server/components.yml
```

## Change Log
The following lines are commented out from the metrics-server deployment manifest v0.6.4: https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml
- lines 142 to 148
```
        livenessProbe:
          failureThreshold: 3
          httpGet:
            path: /livez
            port: https
            scheme: HTTPS
          periodSeconds: 10
```
- lines 154 to 161
```
        readinessProbe:
          failureThreshold: 3
          httpGet:
            path: /readyz
            port: https
            scheme: HTTPS
          initialDelaySeconds: 20
          periodSeconds: 10
```

In addtion, the parameter metric-resolutionis set to 60s on line 139. OKE Virtual Nodes support a minimum metric resolution of 60 seconds.
```
        - --metric-resolution=60s
```

Previously, the following lines were commented out from the metrics-server deployment manifest v0.6.3.
- lines 142 to 148
- lines 154 to 161
- lines 167 to 170
