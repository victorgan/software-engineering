# Dynamic Provisioning

> <- Back to [[K8s Storage]]

Automatically creating storage volumes when a PVC is created, without requiring an admin to pre-provision PVs. The StorageClass's provisioner (e.g., kubernetes.io/aws-ebs) creates the actual cloud storage resource. Simplifies operations and enables developer self-service for storage needs.

#cloud #containers #kubernetes #storage
