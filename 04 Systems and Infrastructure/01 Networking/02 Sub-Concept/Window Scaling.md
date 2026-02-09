# Window Scaling

> <- Back to [[Flow Control]]

A TCP option (RFC 7323) that extends the 16-bit window size field beyond its 65,535-byte limit. The scaling factor (up to 14) is negotiated during the handshake, allowing windows up to ~1 GB. Essential for high-bandwidth, high-latency connections (e.g., transatlantic links).

#networking #tcp #performance
