# Idempotent Tasks

> <- Back to [[Ansible]]

Ansible modules check the current state before making changes. If the desired state already exists, no action is taken. Running the same playbook multiple times is safe and produces the same result. This idempotency is fundamental — it means playbooks can be re-run after failures without side effects.

#cloud #iac
