# Bridge Networks

> <- Back to [[Container Networking]]

The default Docker network mode. Creates a virtual bridge on the host, and each container gets a virtual ethernet interface connected to it. Containers on the same bridge can communicate via IP. Port mapping (-p 8080:80) exposes container ports to the host. Provides network isolation between containers.

#cloud #containers #networking
