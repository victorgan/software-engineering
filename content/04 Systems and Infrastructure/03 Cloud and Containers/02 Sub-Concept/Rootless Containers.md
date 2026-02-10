# Rootless Containers

> <- Back to [[Container Security]]

Running containers without requiring root privileges on the host. Uses user namespaces to map container root to an unprivileged host user. Significantly reduces the security impact of container escapes. Supported by Docker (rootless mode), Podman (rootless by default), and Kubernetes (since 1.22).

#cloud #containers #security
