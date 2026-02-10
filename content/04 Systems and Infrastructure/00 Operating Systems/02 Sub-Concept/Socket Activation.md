# Socket Activation

> <- Back to [[systemd]]

systemd can listen on sockets on behalf of services and start the service only when a connection arrives. This enables on-demand service startup, faster boot times (services start in parallel), and zero-downtime service restarts by passing the listening socket to the new process.

#operating-systems #linux
