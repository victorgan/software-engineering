# Coordination Cost

> <- Back to [[Strong Consistency]]

Strong consistency requires nodes to communicate and agree before responding, adding latency proportional to network round-trip times. This coordination becomes expensive across data centers (50-300ms per round trip). The fundamental reason why many large-scale systems choose weaker consistency models.

#distributed-systems #consistency #performance
