# Values and Templates

> <- Back to [[Helm]]

Templates use Go templating to inject configurable values into Kubernetes manifests. Values can be set via values.yaml (defaults), --set flags, or environment-specific value files (values-prod.yaml). This enables a single chart to deploy across dev, staging, and production with different configurations.

#cloud #containers #kubernetes
