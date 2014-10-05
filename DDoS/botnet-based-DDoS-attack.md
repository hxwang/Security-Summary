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
Botnet can have hundreds of implementation. Based on how bots are controlled by the masters, botnets are classified into three major categories, **IRC-based**, **Web-based** and **P2P-based**. [[Link]](https://github.com/hxwang/Security-Summary/blob/master/DDoS/botnet-types.md)


#### Defense Challenge
According to [[Peng-2007]](http://dl.acm.org/citation.cfm?id=1216373) , there are two main reasons that make the development of an effective DDoS defense mechanism even more challenging when attacker employ zombies to launch DDoS flooding attacks.

- First, A large number of zombies involved in the attack facilitates attackers to make the attacks larger in scale and more disruptive.
- Second, zombies' IP addresses are usually spoofed under the control of the attacker, which makes it very difficult to traceback the attack traffic even to the zombies.
- `My comments: For our designed moving target defense, we can prevent spoofed IP address attack.`

#### Defense 
- Goal
	- detect the attack as soon as possible
	- stop the attack ad near as possible to their source
	
- Defense location	
Different location for performing DDoS detection and response is shown in the following Fig.
![](https://github.com/hxwang/Security-Summary/blob/master/DDoS/botnet-defense-location.PNG)
	- From the figure, we can see that a DDoS flooding attack resembles a funnel in which attack flows are generated in a dispersed area(i.e., source), forming the top of the funnel, receives all the attack flow generated.
	- Thus, detecting a DDoS flooding attack is relatively easier at the destination(victim), since all the flows can be observed at the destination.
	- While it is difficult for an individual source network of the attack to detect the attack unless a large number of attack flows are initiated from that source.
	- Obviously, it is desirable to respond to the attack flows closer to the sources of the attacks, but there is a trade-off between accuracy of the detection and how close to the source of attack the prevention and response mechanism can stop or respond to the attack.

- Defense Mechanism
	- The following figure shows the taxonomy of defense mechanisms against DDoS flooding attacks.
![](https://github.com/hxwang/Security-Summary/blob/master/DDoS/botnet-defense-taxonomy.PNG)

	- If classification by time, then the mechanisms could be before, in, or after the attack. However, a comprehensive DDoS defense mechanism should include all three defenses since there is no one-size-fit-all solution to the DDoS problem.

	- The following figure gives more detail example of location-based defense.
![](https://github.com/hxwang/Security-Summary/blob/master/DDoS/botnet-network-level-defense-by-location.PNG)

