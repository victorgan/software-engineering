# Registry Authentication

> <- Back to [[Container Registries]]

Securing access to container registries using credentials. Docker uses ~/.docker/config.json for credentials. Kubernetes uses imagePullSecrets or service account-based authentication (GKE workload identity, EKS IAM roles). CI/CD pipelines need push credentials; runtime environments need pull credentials.

#cloud #containers #security
