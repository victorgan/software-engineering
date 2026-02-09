# Congestion Avoidance

> <- Back to [[Congestion Control]]

After slow start reaches the threshold, the congestion window grows linearly (additive increase) instead of exponentially. On packet loss, the window is reduced (multiplicative decrease). This AIMD (Additive Increase, Multiplicative Decrease) behavior probes for available bandwidth while quickly backing off on congestion.

#networking #tcp #performance
