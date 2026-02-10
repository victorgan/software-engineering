# Receiver Window

> <- Back to [[Flow Control]]

The amount of data the receiver is willing to accept, advertised in each ACK packet. When the receiver's buffer fills up, it advertises a zero window, causing the sender to pause. The receiver opens the window again when buffer space is available, resuming data flow.

#networking #tcp
