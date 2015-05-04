## Examples


- Periodiacallly change the operating of a system that provides a critical service, to make it harder for attackers to exploit a specific OS's known vulnerabilities. [[Mrco-2014]](http://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=6798537)
- Restructruing a software-defined network's topology, which could disrupt attacks amounted through compromised nodes in the subne. [[Mrco-2014]](http://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=6798537)
- Changeing the address space layout to disrupt precoded buffer-overflow. [[Mrco-2014]](http://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=6798537)

- ASLR
  - OS developers have used it in production system at Apple, Microsoft, and Linux for several years.
  - ASLR involes randomly arranging the memory layout of the process's address space to make it harder for an adversary to execute attacks that rely, for example, on executing return-to-libc or inhected shellcode on the stack. ALSR doesn't make it impossible to conduct such attacks, but it greatly increases the cost for executing the attack. [[Mrco-2014]](http://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=6798537)

### Network-based (IP/Port Change)
Most work on network-based MTDS focuses on low-level techniques such as IP address shifting and network routing and topology control.
- In the late 90s, BBN developed approaches to active network defense [[Kewley-2001]](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=932214) that gave the illusion that the addresses and port numbers used by the network's computer changed dynamically.
  - While these techniques significantly increased the attackers' effort by making it almost impossible to map the network, they required all trusted computers be shield by special process and has several application interoperability issues.
- In [[Antonatos-2007]](http://dl.acm.org/citation.cfm?id=1103633), a network address space randomization scheme to thwart hit worms is proposed, which configured DHCP servers to
- IP-Hop-ping. 
  - IP-Hopping relies on changing a host's IP address to increase the complexity of network attacks such as communication eavesdropping and hijacking. By changing network address, most of the standard techniques for flow and session isoalation will likedly be disrupted, greatly increasing the complexity of mounting a successful attack. [[Mrco-2014]](http://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=6798537)
