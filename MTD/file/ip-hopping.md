## IP Hopping

### Intro
- IP-Hopping relies on changing a host's IP address to increase the complexity of network attacks such as communication eavesdropping and hijacking. By changing network address, most of the standard techniques for flow and session isoalation will likedly be disrupted, greatly increasing the complexity of mounting a successful attack. [[Mrco-2014]](http://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=6798537)


  
### Transparent Host Mutation
- [[Jafarian12]](https://www.ece.cmu.edu/~ece739/papers/movingtarget.pdf)
- Goal: IP address randomization in a LAN using OpenFlow protocol
- How it works
  - In the OenFlow protocol, network switches can be configured as high-speed network caches. When the swtich receives a packet and does not know how to forward the packet, it can ask for instrauctions (called elevation) from a specific machine, called the OpenFlow Controller.
  - The OpenFlow mutation approach uses this elevation mechanism to alter the DNS records and to change packet address in flight. 
    - When a client performs a DNS lookp, the DNS server will provide the client with a virtual IP address for a target. 
    - When the client attempts to access the target, the packet is forward using the virtual IP address until it reaces the destination swtich, at which point it is translated to the destionation host's IP address.
    - The network swtiches essentially act as NAT devices, performing translations between virtual and real IP addresss.
  - THe OpenFlow controller essentially servers as the mapping system. The controller updates the DNS server with different virtual IP address for each system and orders the OpenFlow swtiches to install NAT rules to hide the identities of both hosts. Unfortunately, since the OpenController must have control of the resource and destination switch, the approach is most suited to a LAN.
- Weakness
  - modify network infrstructure?
  
### MT6D
- [[DunLop11]](http://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=6127486)
- Goal:
- How it works
  - The client and the target share a symmetric key out-of-band and uses these keys to determine the IPv6 addresses the hosts will use. 
  - To construct their IPv6 addresses, the hosts construct a hash using the shared key, a value derived from the hosts' MAC address and a timestamp. The approach extracts 64 bits from the hash output to encode the lower 64 bits of the host's IPv6 address. 
  - To provide uniform communication between the host applications, the operating system on each host users a tunneling approach and rotates the address of the tunnel end-points. 
- Weakness
  - modified both end-hosts of communicate-end to coordinate their movements
