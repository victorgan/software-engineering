# Firewall Rules

> <- Back to [[NAT Firewalls and VPNs]]

Rules that permit or deny network traffic based on source/destination IP, port, and protocol. iptables/nftables on Linux, security groups in AWS/GCP. Best practice: default deny all, explicitly allow required traffic. Stateful firewalls track connection state to allow return traffic automatically.

#networking #security #infrastructure
