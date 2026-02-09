# Slow Start

> <- Back to [[Congestion Control]]

TCP begins with a small congestion window (typically 10 segments) and doubles it every RTT until packet loss occurs or a threshold is reached. Despite the name, growth is exponential — "slow" only compared to sending at full rate immediately. Affects initial page load times significantly.

#networking #tcp #performance
