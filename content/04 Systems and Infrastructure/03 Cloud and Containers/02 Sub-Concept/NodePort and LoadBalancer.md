# NodePort and LoadBalancer

> <- Back to [[K8s Networking]]

NodePort exposes the service on a static port on every node's IP, accessible externally via node-ip:port. LoadBalancer provisions a cloud load balancer (ALB, NLB, GCE LB) that routes external traffic to the service. LoadBalancer is the standard way to expose services to the internet in cloud environments.

#cloud #containers #kubernetes #networking
