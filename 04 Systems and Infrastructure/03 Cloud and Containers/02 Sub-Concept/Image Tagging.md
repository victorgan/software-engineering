# Image Tagging

> <- Back to [[Container Registries]]

Tags identify specific versions of an image (e.g., myapp:v1.2.3, myapp:latest). Best practices: use semantic version tags for production (immutable), avoid relying on :latest (mutable, unpredictable). Use digest-based references (sha256:abc...) for guaranteed immutability in deployments.

#cloud #containers
