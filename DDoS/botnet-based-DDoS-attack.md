Botnet-based DDoS attack
---

- Note: contents of this page are from paper [[Zigzar-2013]]()

#### Trend
Botnets are the dominant mechanisms that facilitate DDoS flooding attacks on computer networks or applications. Most of the recent and most problematic application layer DDoS flooding attacks have employed botnets.


#### Botnet Intro
- Usually a group of zombies that are controlled by an attacker(a.k.a. Master) form a botnet. Botnets consist of masters, handlers, and bots(a.k.a. Agents), depicted in the following Figure.

#### Defense Challenge
According to [[Peng-2007]](http://dl.acm.org/citation.cfm?id=1216373) , there are two main reasons that make the development of an effective DDoS defense mechanism even more challenging when attacker employ zombies to launch DDoS flooding attacks.

- First, A large number of zombies involved in the attack facilitates attackers to make the attacks larger in scale and more disruptive.
- Second, zombies' IP addresses are usually spoofed under the control of the attacker, which makes it very difficult to traceback the attack traffic even to the zombies.
- `My comments: For our designed moving target defense, we can prevent spoofed IP address attack.`

