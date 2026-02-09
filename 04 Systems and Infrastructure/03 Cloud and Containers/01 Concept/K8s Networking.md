# K8s Networking

> <- Back to [[Container Orchestration]]

Kubernetes networking model: every pod gets its own IP, pods can communicate directly without NAT, and services provide stable endpoints. Service types: ClusterIP (internal only), NodePort (exposed on node ports), LoadBalancer (cloud LB). Network policies control traffic flow between pods.

## Key Properties

- [[ClusterIP Service]]
- [[NodePort and LoadBalancer]]
- [[Network Policies]]

## Related

- [[Kubernetes]] (networking is a core K8s concept)
- [[Container Networking]] (underlying networking primitives)
- [[Service Mesh on K8s]] (advanced traffic management)

---

#cloud #containers #kubernetes #networking
