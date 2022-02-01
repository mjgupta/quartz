---
title: "TCP"
---
[Wiki](https://en.wikipedia.org/wiki/Transmission_Control_Protocol)
### Congestion control
- [TCP Cubic](TCP%20Cubic.md)
- [TCP BBR](TCP%20BBR.md)
[Wiki](https://en.wikipedia.org/wiki/TCP_congestion_control)
#### TCP over wireless networks
- TCP was originally designed for wired networks. Packet loss is considered to be the result of network congestion and the congestion window size is reduced dramatically as a precaution.
- However, wireless links are known to experience sporadic and usually temporary losses due to fading, shadowing, hand off, interference, and other radio effects, that are not strictly congestion. After the (erroneous) back-off of the congestion window size, due to wireless packet loss, there may be a congestion avoidance phase with a conservative decrease in window size. This causes the radio link to be underutilized. 
- Extensive research on combating these harmful effects has been conducted. Suggested solutions can be categorized as end-to-end solutions, which require modifications at the client or server, link layer solutions, such as Radio Link Protocol (RLP) in cellular networks, or proxy-based solutions which require some changes in the network without modifying end nodes.

#networking 
#congestioncontrol 