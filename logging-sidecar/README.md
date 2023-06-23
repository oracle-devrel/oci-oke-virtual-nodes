# Kubernetes pod with a sidecar for logging 
The purpose of this manifest is to show how to add a sidecar to pod to send logs on a flat file to a persistent location such as Opensearch.

To deploy the manifest, run the command:
```
kubectl apply -f https://raw.githubusercontent.com/oracle-devrel/oci-oke-virtual-nodes/main/date-logging.yaml
```
