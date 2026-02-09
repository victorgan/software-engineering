# Continuous Reconciliation

> <- Back to [[GitOps]]

GitOps tools continuously compare the desired state in Git with the actual cluster state. If drift is detected (manual changes, failed deployments), the tool automatically reconciles by reapplying the Git configuration. This self-healing behavior ensures the cluster always matches the declared configuration.

#cloud #iac #gitops
