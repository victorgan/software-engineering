# Network Policies

> <- Back to [[K8s Networking]]

Rules that control which pods can communicate with each other and with external endpoints. By default, all pods can communicate with all other pods. Network policies use label selectors to define ingress and egress rules. Requires a CNI plugin that supports policies (Calico, Cilium, Weave).

#cloud #containers #kubernetes #networking #security
