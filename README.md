# oci-oke-virtual-nodes

[![License: UPL](https://img.shields.io/badge/license-UPL-green)](https://img.shields.io/badge/license-UPL-green) [![Quality gate](https://sonarcloud.io/api/project_badges/quality_gate?project=oracle-devrel_oci-oke-virtual-nodes)](https://sonarcloud.io/dashboard?id=oracle-devrel_oci-oke-virtual-nodes)

## Introduction
OKE virtual nodes deliver a complete serverless Kubernetes experience. With virtual nodes, you can ensure reliable operations of Kubernetes at scale without needing to manage any worker node infrastructure. Virtual nodes provides granular pod-level elasticity and pay-per-pod pricing, while eliminating the operational overhead of managing, scaling, upgrading, and troubleshooting worker nodes’ infrastructure. 

OKE virtual nodes does not currently support all specs in deployment manifests. For more information, refer to [Virtual Nodes and Virtual Node Pools](https://docs.oracle.com/en-us/iaas/Content/ContEng/Tasks/contengcomparingvirtualwithmanagednodes_topic.htm#contengcomparingvirtualwithmanagednodes_topic-virtualnodes). This repository includes examples of modified manifests for common software packages.

## Getting Started
### Deploy metrics server in a cluster with virtual nodes
```
kubectl apply -f https://raw.githubusercontent.com/oracle-devrel/oci-oke-virtual-nodes/main/metrics-server/components.yml
```
### Deploy Nginx Ingress Controller in a cluster with virtual Nodes
```
kubectl apply -f https://raw.githubusercontent.com/oracle-devrel/oci-oke-virtual-nodes/main/ingress-nginx/deploy.yaml
```

# Prerequisites
- You have an Oracle Cloud Infrastructure (OCI) account. Get started with Oracle Cloud Infrastructure today with our [Oracle Cloud Free Trial](https://www.oracle.com/cloud/free/).
- A Kubernetes cluster is created with Oracle Container Engine for Kubernetes (OKE). For more information, refer to [Creating Kubernetes Clusters](https://docs.oracle.com/en-us/iaas/Content/ContEng/Tasks/contengcreatingclusterusingoke.htm).
- The Kubeconfig file is configured to access the Kubernetes cluster. For more information, refer to [Accessing a Cluster Using Kubectl](https://docs.oracle.com/en-us/iaas/Content/ContEng/Tasks/contengaccessingclusterkubectl.htm).

## Notes/Issues
* Nothing at this time

## URLs
* Nothing at this time

## Contributing
This project is open source.  Please submit your contributions by forking this repository and submitting a pull request!  Oracle appreciates any contributions that are made by the open source community.

## License
Copyright (c) 2022 Oracle and/or its affiliates.

Licensed under the Universal Permissive License (UPL), Version 1.0.

See [LICENSE](LICENSE) for more details.

ORACLE AND ITS AFFILIATES DO NOT PROVIDE ANY WARRANTY WHATSOEVER, EXPRESS OR IMPLIED, FOR ANY SOFTWARE, MATERIAL OR CONTENT OF ANY KIND CONTAINED OR PRODUCED WITHIN THIS REPOSITORY, AND IN PARTICULAR SPECIFICALLY DISCLAIM ANY AND ALL IMPLIED WARRANTIES OF TITLE, NON-INFRINGEMENT, MERCHANTABILITY, AND FITNESS FOR A PARTICULAR PURPOSE.  FURTHERMORE, ORACLE AND ITS AFFILIATES DO NOT REPRESENT THAT ANY CUSTOMARY SECURITY REVIEW HAS BEEN PERFORMED WITH RESPECT TO ANY SOFTWARE, MATERIAL OR CONTENT CONTAINED OR PRODUCED WITHIN THIS REPOSITORY. IN ADDITION, AND WITHOUT LIMITING THE FOREGOING, THIRD PARTIES MAY HAVE POSTED SOFTWARE, MATERIAL OR CONTENT TO THIS REPOSITORY WITHOUT ANY REVIEW. USE AT YOUR OWN RISK. 
