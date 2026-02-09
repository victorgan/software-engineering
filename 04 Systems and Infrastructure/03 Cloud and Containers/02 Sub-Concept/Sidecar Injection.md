# Sidecar Injection

> <- Back to [[Service Mesh on K8s]]

The service mesh control plane automatically injects a proxy sidecar container into every pod, typically via a mutating admission webhook. When a pod is created in a mesh-enabled namespace, the webhook modifies the pod spec to include the proxy container. No application code changes required.

#cloud #containers #kubernetes #service-mesh
