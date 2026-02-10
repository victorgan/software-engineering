# Cluster Autoscaler

> <- Back to [[K8s Scaling]]

Automatically adjusts the number of nodes in the cluster. Adds nodes when pods cannot be scheduled due to insufficient resources; removes underutilized nodes to save cost. Works with cloud providers' managed node groups (AWS ASG, GKE node pools). Must coordinate with HPA for effective autoscaling.

#cloud #containers #kubernetes #scaling
