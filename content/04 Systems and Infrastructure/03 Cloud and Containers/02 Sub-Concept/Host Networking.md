# Host Networking

> <- Back to [[Container Networking]]

The container shares the host's network namespace directly — no network isolation. The container uses the host's IP address and ports. Best performance (no NAT overhead) but sacrifices isolation. Useful for network-intensive applications or when port mapping overhead is unacceptable.

#cloud #containers #networking
