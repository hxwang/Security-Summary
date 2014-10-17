## Moving Target Defense Technical Type


### Network-based
Most work on network-based MTDS focuses on low-level techniques such as IP address shifting and network routing and topology control.
- In the late 90s, BBN developed approaches to active network defense [[Kewley-2001]](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=932214) that gave the illusion that the addresses and port numbers used by the network's computer changed dynamically.
  - While these techniques significantly increased the attackers' effort by making it almost impossible to map the network, they required all trusted computers be shield by special process and has several application interoperability issues.
- In [[Antonatos-2007]](http://dl.acm.org/citation.cfm?id=1103633), a network address space randomization scheme to thwart hit worms is proposed, which configured DHCP servers to expire the leases of hosts at various intervals to support address randomization. 
