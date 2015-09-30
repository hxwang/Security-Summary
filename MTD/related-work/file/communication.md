## Communication Diversificaiton

- [ref](http://dl.acm.org/citation.cfm?id=2663486)

Techqniues of communication diversification protect systesm against netowrk related attacks, in way to hide internal information or communication protocols.
- Christodorescu et al. propose to **change the internal** of a system, aiming at defeinding attacks that rely on internals of a system, aiming at defending attacks that rely on internal knowledge of the system.
  - For instance, periodidcally alterning the schema of the database of a website, such as challenging table titles, could mitigate SQL injections but without causing service failures.
- The Mutable Netowrks (MUTE) defense architecture propsoed by Al-Shaer enables systems to automatically **change communication configuration**, and thus reduce advesary's capabilities in target scanning and exploiting. 
  - With IP randomization, a network would change its IP address frequentlym and only synchronized new IP addresses with authroized users. hence, attackers are segregated from the network. 
- Another techqniue called Random Finger Printing in MUTE enables a system to interpret and **modify its response to outside** requests. Fake information of a system exposed to the public, such as OS type and application identity, and such information could hinder remote exploitation.
