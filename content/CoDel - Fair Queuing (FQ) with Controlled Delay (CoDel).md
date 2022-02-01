---
title: "CoDel - Fair Queuing (FQ) with Controlled Delay (CoDel)"
---
### How it works

CoDel assumes transient queuing is acceptable, a small amount of standing queue is acceptable, and that it is unacceptable to drop when there are fewer than an MTU worth of bytes in the buffer. CoDel determines standing queue by tracking the minimum packet delay through a buffer over a sliding time window, where the window is on the order of a round trip time (delay measured at each packet's departure as its time spent in the buffer). If the minimum packet delay exceeds the small target standing queue for longer than a time interval on the order of a round trip time, a packet is dropped and a control law used to set the next drop time. As soon as a packet delay at or below target is seen, drops are canceled. This ensures that delay must have persisted for a network-significant amount of time.

Using **packet time spent enqueued as the input to the local congestion controller** results in an AQM that works at any link bandwidth, including one that is time varying. Target and interval are constants: acceptable queue delay (to prevent starvation) and a time on the order of a worst case RTT of connections through the bottleneck. Tracking the recently experienced standing queue means CoDel reacts to congestion and its removal in a timely fashion and does not make drops that "starve" the buffer.

#### MAN Page
FQ_Codel (Fair Queuing Controlled Delay) is queuing discipline that combines Fair Queuing with the CoDel AQM scheme. FQ_Codel uses a stochastic model to classify incoming packets into different flows and is used to provide a fair share of the bandwidth to all the flows using the queue.
Each such flow is managed by the CoDel queuing discipline. Reordering within a flow is avoided since Codel internally uses a FIFO queue.

## Outlines
##### CoDel
- Active queue management (AQM) algorithm in network routing
- Designed to overcome [BufferBloat](BufferBloat.md) in networking hardware, such as routers, by setting limits on the delay network packets experience as they pass through buffers in this equipment.
##### FQ Codel
- Flow Queue CoDel

## Predessecors
- [Random early detection](https://en.wikipedia.org/wiki/Random_early_detection)
- [Codel vs RED](https://queue.acm.org/detail.cfm?id=2209336)
## Advances
- [The Cake Algoritm](The%20Cake%20Algoritm.md)

## References
[Controlled Delay](https://datatracker.ietf.org/doc/rfc8289/)
[FqCodel](https://datatracker.ietf.org/doc/rfc8290/)
[Wikipedia](https://en.wikipedia.org/wiki/CoDel)
[IETF](https://www.ietf.org/blog/codel-improved-networking-through-adaptively-managed-router-queues/)

#networking 
#ActiveQueueManagement
#QueueManagement 