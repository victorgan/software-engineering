# ConfigMaps and Secrets K8s

> <- Back to [[Kubernetes]]

ConfigMaps store non-sensitive configuration data as key-value pairs, mountable as files or environment variables. Secrets store sensitive data (passwords, tokens) with base64 encoding (not encryption by default — use external solutions or encrypted etcd for true security). Both decouple configuration from container images.

#cloud #containers #kubernetes
