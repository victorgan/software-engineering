# Collapsed Forwarding

> <- Back to [[Origin Shield]]

When multiple edge servers simultaneously request the same uncached content, the shield coalesces these into a single origin request. The first request is forwarded to the origin; subsequent requests for the same content wait for the first response. Also called request coalescing or deduplication.

#networking #cdn #performance
