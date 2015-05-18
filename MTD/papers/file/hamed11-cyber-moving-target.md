## [Achieving Cyber Survivability in a Contested Environment Using a Cyber Moving Target](https://www.ll.mit.edu/mission/cybersec/publications/publication-files/full_papers/2011_05_01_Okhravi_HighFrontier_FP.pdf)

### Summary
In this paper, the authors discuss their design of a moving target defense mechanism -- TALENT. Note different from traditional VM migration which has homogeneous operating system, they can support heterogeneous system.

The authors also introudce NetSPA, their designed attack-graph generation and reachability analysis tool. 
- It requires only a few core pieces of knowledge to build a an attack graph. 
  - For a given host, the tool must know which credentials can be acquired at a given access level on the host and which ports the host can reach.
  - For a given port, NetSPA requires knowledge of the port's vulnerabilities.
  - For each instastance of vulnerability, the tool must know which is required to exploit it and what is gained by exploiting it.
  


### Comment
- The parts about attack graph generation and reachability analysis is intersting. We can further consider design strategy to better prevent reachability.
