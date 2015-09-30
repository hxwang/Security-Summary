## Definition of Moving Target Defense


### Definition
- Moving Target Defense(MTD) is the concept of controlling change across multiple system dimensions in order to increase uncertinaty and apparent complexity for attackers, reduce their window of opportunity and increase the costs of their probing and attack efforts [[DHS-GOV-2011]](http://www.dhs.gov/csd-mtd)
- MTD can be thought simply as constantly changing a computer system to reduce or move the exploitable attack surface, which are the resources available to attackers (e.g., software, ports, component vulnerabilities, etc) that can be used to compromise the system. [[Zhuang15]](http://people.cis.ksu.edu/~sdeloach/publications/Conference/MTD15-attacktheory.pdf)

### [Motivation](file/motivation.md)

### Benefits
- MTD techniques generally focus not on the shields that protect the targes but on the manipulation and control of the targets themselves, to create the perception of movement to attackers. The goal is to mitigate the assymmetric advantage of attackers by increasing the complexity, diversity, and uncertainty over the protected system's attack surface. [[Mrco-2014]](http://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=6798537)
- The point of dynamically modifying the runtime environment is that specific knowledge that the attacker has accumulated from probes to that point (e.g., based on specific memory locations of attack surfaces) is *rendered obsolete* by the runtime modification.

### Categories
- Proactive v.s. Reactive [ref](http://ieeexplore.ieee.org/xpl/articleDetails.jsp?reload=true&arnumber=6900086)
  - Proactive MTD
    - In protactive MTD, possible adversrial behaviros are anticipated, and the corresponding defensive strategies are incorporated int othe system design to thwart attacks proactively without disrupting operations.
    - In addition, some elements of the defense system, such as Interent protocol (IP) addresses, port numbers, operating systems, etc., are diversified periodically to create a varying attack surface.
  - Reactive MTD
    - In reactive MTD, systems react out of necessity to defend against a detected malicious attack.
  

### [Examples](file/example.md)



### Research problems
- Adaptation Selection Problem [[Zhuang15]](http://people.cis.ksu.edu/~sdeloach/publications/Conference/MTD15-attacktheory.pdf)
  - How to select the next configuration state?
- Timing Problem [[Zhuang15]](http://people.cis.ksu.edu/~sdeloach/publications/Conference/MTD15-attacktheory.pdf)
  - When to carry out the adaptation 
