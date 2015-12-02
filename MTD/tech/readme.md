## MTD techniques

### Category 1: Network Level MTD
- MAC layer: changing MAC address
- IP Layer: IP randomization
  - [IP-Hop-ping](../file/ip-hopping.md)
- TCP layer: changing network protocol
- Session layer
- Other
  - Restructruing a software-defined network's topology, which could disrupt attacks amounted through compromised nodes in the subne. [[Mrco-2014]](http://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=6798537)

- **wireless frequency hopping**
  - used to avoid jammers [[Green15]](http://arxiv.org/pdf/1404.6785.pdf)

### Category 2: System Level MTD
- Hardware-based
  - Processor, FPGA
- Software-based
  - Application, OS, Data
    - Periodiacallly change the operating of a system that provides a critical service, to make it harder for attackers to exploit a specific OS's known vulnerabilities. [[Mrco-2014]](http://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=6798537)


### Category 3: Application Level MTD
- Changeing the address space layout to disrupt precoded buffer-overflow. [[Mrco-2014]](http://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=6798537)
- ASLR
  - OS developers have used it in production system at Apple, Microsoft, and Linux for several years.
  - ASLR involes randomly arranging the memory layout of the process's address space to make it harder for an adversary to execute attacks that rely, for example, on executing return-to-libc or inhected shellcode on the stack. ALSR doesn't make it impossible to conduct such attacks, but it greatly increases the cost for executing the attack. [[Mrco-2014]](http://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=6798537)




 

