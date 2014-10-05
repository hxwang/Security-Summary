Defense mechanisms against network/transport-level DDoS attacks(Source based mechanisms)
---

- Note: contents of this page are from paper [Zigzag-2013]()

Source-based mechanisms are deployed near the sources of the attack to prevent network customers from generating DDoS flooding attacks.  These mechanism can either take place either at the **edge routers** of the source's local network or at the **access routers** of an Autonomous System(AS) that connects to the sources' edge routers[[Criscuolo-2000]](http://www.iwar.org.uk/comsec/resources/reports/CIAC-2319_Distributed_Denial_of_Service.pdf). 

### Ingress/Egress filtering at the sources' edge routers[[Ferguson-2000]](http://dl.acm.org/citation.cfm?id=RFC2827)
- how it works
	- The current IP protocol allows source hosts to alter source addresses in the IP packets. Victims cannot distinguish attack packets from legitimate ones based on source addresses. Although the IPSec protocol [[RFC2402-1998]](https://tools.ietf.org/html/rfc2402) can address this problem by authenticating the source addresses of IP packets, this method is not widely deployed among service providers because of its increased overhead.
	- Ingress/Egress filtering mechanisms have been proposed to detect and filter packets with **spoofed IP address** at the **source's edge routers* based on the valid IP address range internal to the network.
- drawback
	- cannot detect if the spoofed IP addresses are still in the valid internal IP address range.
	- under the filter mechanism, mobile IP address has to be tunnelled in order to avoid filtering.
	- considering the current trend towards employing botnets to launch various atacks, attackers can still attack their targets by employing the pool of zombies with genuine IP addresses available through botnets. 
	
### D-WARD
- [[Mirkovic-2002]](ftp://im1.im.tku.edu.tw/assistant/bearhero/attacking-ddos-at-the-source.pdf)
  [[Mirkovic-2003]](http://www.isi.edu/~mirkovic/publications/nca03.pdf)
- How it works
	- This scheme aims to detect DDoS flooding attack traffic by monitoring both inbound and outbound traffic of a source network and comparing the network traffic information with **predefined normal flow models**. Attack flows are identified and filtered if they mismatch the normal flow models. 
	- D-WARD attempts to stop attack traffic originating from a network at the border of the source network.
	- For instance, in the TCP protocol, every packet will be acknowledged by the receiver. Hence, the normal traffic model for TCP flow could be defined by a maximum allowed ratio ofthe number of packets sent and received in the aggregate TCP flow to the peer. A normal model for all other traffic types could be defined in a similar way. 
- Drawback
	- it consumes more memory space and CPU cycles than some ofthe network-based defense mechanisms. 
	- there is **no strong incentives** for the providers to employ D-WARD as it protects the other's network but not the providers' network from DDoS flooding attack.
	- it can be easily bypassed by attackers who can control their traffic to be within a normal range.

### Multi-Level Tree for Online Packet Statistics(MULTOPS) and Tabulated Online Packet Statistics(TOPS)
- [[MULTOPS-2001]](http://www.utdallas.edu/~kxs028100/Papers/multops.pdf)
[[TOPS-2003]](http://ieeexplore.ieee.org/xpl/login.jsp?tp=&arnumber=1258459&url=http%3A%2F%2Fieeexplore.ieee.org%2Fxpls%2Fabs_all.jsp%3Farnumber%3D1258459)

- How it works
	- MULTOPS is a heuristic and a data-structure that network devices(e.g., routers) at the source subnet can use to detect and filter DDoS flooding attacks.
	- Normallly the rate of **traffic in one direction is proportional to that in the opposite direction during normal operations on the Internet** [[MULTOPS-2001]](http://www.utdallas.edu/~kxs028100/Papers/multops.pdf).
	- Hence, a significant difference between the rates of traffic going to and coming from a host or subnet can indicate that the network prefix is either the source or the destination of an attack.
	- An alternative approach called TOPS provides an efficient method for detecting packet flow imbalance based on a hashing scheme that uses a small set of field length lookup tables. TOPS can improve the accuracy and reduce the false alarms rate of the system by monitoring traffic by protocol, and maintaining a probability distribution of traffic flow rates. 
- Drawback
	- MULTOPS uses a dynamic tree structure for monitoring packet rates for each IP address which makes it a vulnerable target for a memory exhaustion attack [[MULTOPS-2001]](http://www.utdallas.edu/~kxs028100/Papers/multops.pdf). 
	- Both MULTOPS and TOPS are based on the **assumption** that incoming and outgoing traffic rates are proportional, which is not always the case. For instance, rates for multimedia streams are not proportional and significantly higher than the ones from clients. Hence, MULTOPS and TOPS can have high false negative rates. 
	- Furthermore, attackers can increase the proportion ofthe incoming and outgoing traffic rates legitimately (e.g., downloading large files from different fup servers through a number of genuine sources); hence during the attack, the attack trffic will be undtected because of the similarity of the attack traffic rates to the normal traffic rates which have been legitimately increased.

	
