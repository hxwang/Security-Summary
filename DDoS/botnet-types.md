#### BotNet Types
Botnet can have hundreds of implementation. Based on how bots are controlled by the masters, botnets are classified into three major categories, IRC-based, Web-based and P2P-based. 

##### IRC-based
- Ref: [[Lo-1997]](http://www.irchelp.org/irchelp/irctutorial.html)
- IRC is an on-line text-based instant messaging protocol in the Internet.  It has client/server architecture with default channels to communicate between servers.
- Convenient for attacker to use
    - IRC can connect to hundreds of clients via multiple servers. 
    - Using IRC channels as handles, attackers can use legitimate IRC ports to send commands to the bots making it much more difficult to track the DDoS command and control structure. 
    - Furthermore, an attacker can easily hides its presentce because of the large volume of traffic that IRC servers usually have.
    - Additionally, an attacker can easily share files to distribute the malicious code.
    - Moreover, attackers can simply log on to the IRC server and see the list of all available bots instead of maintaining their list locally at their site.
- Limitation
    - the servers are a potential central point of failure, i.e., the entire botnet can be shutdown if the defender captures the C&C servers. 
- Tool
Several IRC-based botnet tools have been developed and used over the years for launching DDoS attacks such as 
    - [Trinity v3 ](http://www.deepdyve.com/lp/elsevier/trinity-v3-a-ddos-tool-hits-the-streets-SHmJZi62Y6), conduct UDP, TCP SYN, TCP ACK, and TCP NUL flood attacks
    - [Kaiten-Knight.c](http://packetstormsecurity.com/files/23939/knight.c.html), conducts UDP, TCP, SYN and PUSH+ACH flood attacks
    
    
 #### Web-based (a.k.a HTTP-based)
 More recently, botnets have started using HTTP as a communication protocol to send commands to the bots making it much more difficult to track the DDoS command and control structure.
 
 - Characteristic
    - Web-based botnest do not maintain connections with a C&C server like IRC-based botnets do. 
    - Instead, each Web bot periodically downloads the instructions using web requests. Web-based botnets are stealthier since they hide themselves within legitimate HTTP traffic.
    - Bots are configurated and controoled through complex PHP scripts and they use encrypted communication over HTTP( port 80) or HTTPS( port 443) protocol. 
- Tool
Three well known and widely-used web-based botnet tools are
    - [BlackEnergy](http://www.arbornetworks.com/asert/2007/10/blackenergy-ddos-bot-analysis-available/)
    - [Low-Orbit Ion Cannon(LOIC)](https://github.com/neweracracker/loic)
    - [Aldi](http://www.arbornetworks.com/asert/2012/02/ddos-tools/)
    
    
 