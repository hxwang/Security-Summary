Defense mechanism against network/transport-level DDoS attacks
---

### 1. Source based mechanisms
Source-based mechanisms are deployed near the sources of the attack to prevent network customers from generating DDoS flooding attacks.  These mechanism can either take place either at the **edge routers** of the source's local network or at the **access routers** of an Autonomous System(AS) that connects to the sources' edge routers[[Criscuolo-2000]](http://www.iwar.org.uk/comsec/resources/reports/CIAC-2319_Distributed_Denial_of_Service.pdf). 

##### Ingress/Egress filtering at the sources' edge routers[[Ferguson-2000]](http://dl.acm.org/citation.cfm?id=RFC2827)
- how it works
	- The current IP protocol allows source hosts to alter source addresses in the IP packets. Victims cannot distinguish attack packets from legitimate ones based on source addresses. Although the IPSec protocol [[RFC2402-1998]](https://tools.ietf.org/html/rfc2402) can address this problem by authenticating the source addresses of IP packets, this method is not widely deployed among service providers because of its increased overhead.
	- Ingress/Egress filtering mechanisms have been proposed to detect and filter packets with **spoofed IP address** at the **source's edge routers* based on the valid IP address range internal to the network.
- drawback
	- cannot detect if the spoofed IP addresses are still in the valid internal IP address range.
	- under the filter mechanism, mobile IP address has to be tunnelled in order to avoid filtering.
	- considering the current trend towards employing botnets to launch various atacks, attackers can still attack their targets by employing the pool of zombies with genuine IP addresses available through botnets. 
