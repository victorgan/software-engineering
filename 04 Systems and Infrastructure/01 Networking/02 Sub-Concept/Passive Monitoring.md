# Passive Monitoring

> <- Back to [[Health Checks]]

Monitoring actual request responses to detect backend failures without sending additional probe requests. If a backend returns too many 5xx errors or connection timeouts, it is marked unhealthy. Lower overhead than active probing but only works when traffic is flowing.

#networking #load-balancing #reliability
