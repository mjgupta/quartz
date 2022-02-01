---
title: "BufferBloat"
---
[Symptoms of bufferbloat-induced congestion](Symptoms%20of%20bufferbloat-induced%20congestion.md)

### Testing Bufferbloat
[Waveform](http://www.waveform.com/tools/bufferbloat)
[DSLReports](http://www.dslreports.com/faq/17930)
#### ELI5 Wifi buffers
If you're connecting over WiFi, there are actually three buffers . Looking at the download path, there is:
1.  A buffer between your cable, DSL, LTE, satellite or fiber modem and your router;
2.  A buffer between your router and the WiFi access point (which may both be in the same physical box);
3.  A buffer between your phone or laptop's WiFi chipset and the actual computer.
[Source](https://www.waveform.com/tools/bufferbloat)
>Criteria 
Web Browsing:
	Download speed > 2 Mbps
	Upload speed > 100 Kbps
	Latency < 500 ms
Audio Calls:
	Download speed > 100 Kbps
	Upload speed > 100 Kbps
	95th Percentile Latency < 400 ms
4K Video Streaming:
	Download speed > 25 Mbps
Video Conferencing:
	Download speed > 10 Mbps
	Upload speed > 5 Mbps
	95th Percentile Latency < 400 ms
Low Latency Gaming:
	Download speed > 10 Mbps
	Upload speed > 3 Mbps
	95th Percentile Latency < 40 ms

## Resources
- [bufferbloat.net](bufferbloat.net)
- [Bufferbloat and Beyond: Removing Performance Barriers in Real-World Networks](https://blog.tohojo.dk/media/bufferbloat-and-beyond.pdf)

#networking 
#QueueManagement 
#ActiveQueueManagement 
#Bufferbloat
