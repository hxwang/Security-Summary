Botnet-based DDoS attack
---

- Note: contents of this page are from paper [[Zigzar-2013]]()

#### Trend
Botnets are the dominant mechanisms that facilitate DDoS flooding attacks on computer networks or applications. Most of the recent and most problematic application layer DDoS flooding attacks have employed botnets.


#### Botnet Intro
- Usually a group of zombies that are controlled by an attacker(a.k.a. Master) form a botnet. Botnets consist of masters, handlers, and bots(a.k.a. Agents), depicted in the following Fig. 1.
![](https://github.com/hxwang/Security-Summary/blob/master/DDoS/botnet-example.PNG)
- *Handler*
    -  The handlers are means of communication that attackers(a.k.a., Master) use to communicate indirectly with their bots (i.e., to command and control their army).
    -  For instance, handlers can be programs installed on a set of compromised devices(e.g., network servers) that attackers communicate with to send commands. However, most of these installed programs leave unique footprints behind that are detectable with current antivirus software.
    - Hence, currently attackers use other methods(e.g., Internet Relay Chat(IRC)) to communicate with their bots in order to send commands and control them.
- *Bots*
    - Bots are devices that have been compromised by the handlers. 
    - Bots are those systems that will eventually carry out the attack on the victim's system.
    
#### BotNet Types
Botnet can have hundreds of implementation. Based on how bots are controlled by the masters, botnets are classified into three major categories, IRC-based, Web-based and P2P-based. [[Link]]()

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

#### Defense Challenge
According to [[Peng-2007]](http://dl.acm.org/citation.cfm?id=1216373) , there are two main reasons that make the development of an effective DDoS defense mechanism even more challenging when attacker employ zombies to launch DDoS flooding attacks.

- First, A large number of zombies involved in the attack facilitates attackers to make the attacks larger in scale and more disruptive.
- Second, zombies' IP addresses are usually spoofed under the control of the attacker, which makes it very difficult to traceback the attack traffic even to the zombies.
- `My comments: For our designed moving target defense, we can prevent spoofed IP address attack.`

