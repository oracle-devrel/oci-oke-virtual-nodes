# Kubernetes pod with a sidecar for logging 
The purpose of this manifest is to show how to add a sidecar to pod to send logs on a flat file to a persistent location such as Opensearch.

Customize the ConfigMap in date-logging.yaml with
- a value for `host`, the IP address of your Opensearch server
- a value for `port`, the port of your Opensearch server (9200 by default)
- a value for `HTTP_User`, the username of of your Opensearch server
- a value for `HTTP_Passwd`, the password of of your Opensearch server

To deploy the manifest, run the command:
```
kubectl apply -f https://raw.githubusercontent.com/oracle-devrel/oci-oke-virtual-nodes/main/date-logging.yaml
```
