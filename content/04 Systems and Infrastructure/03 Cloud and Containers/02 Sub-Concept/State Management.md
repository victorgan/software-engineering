# State Management

> <- Back to [[Terraform]]

Terraform maintains a state file that maps configuration to real infrastructure resources. State enables detecting drift, planning changes, and tracking dependencies. Remote state backends (S3, GCS, Terraform Cloud) enable team collaboration. State locking prevents concurrent modifications. State must be treated as sensitive data.

#cloud #iac #terraform
