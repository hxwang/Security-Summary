DDoS Attack
---

#### Definition
- A distributed denial of service attack involves a very large number of computers all over the network sending data to a single target system that is to be attacked. If the target system is unable to keep up with the deluge of incoming data, then it wil be unable to handle legitimate data that it is being sent, which basically is the same as shutting down the target system as far as legitimate users are concerned [[Chung-2012]](http://www.sigcomm.org/node/3233).
- As a concrete example, if a web server is being sent an overwhelming number of web requests by a botnet, then legitimate users cannot access any content from the web server.

####  Purpose
- DDoS flooding attacks are typically explicit attempts to disrupt legitimate users' access to services.
- They try to make the victim's services unavailable, leading to revenue losses and increased costs of mitigating the attacks and restoring the services.

####  DDoS attack Types
Currently, there are two methods to launch DDoS attack in the Internet. 

1. The attacker can send some malformed packets to the victim to confuse a protocol or an application running on it(i.e., vulnaribility attack[[Mirkovic-2004]](http://dl.acm.org/citation.cfm?id=997156)).

2. A more common one approach, the attackers trying to do one or both of the following
	- disrupt a legitimate users connectivity by exhuasting **bandwidth**, router processing capacity or network resources; they are essentiallly network/transport-level attacks[[Mirkovic-2004]](http://dl.acm.org/citation.cfm?id=997156), or
	- disrupt a legitimate users' service by exhausting the **server resources** (e.g., sockets, CPU, memory, disk/database bandwidth, and I/O bandwidth); these essentially include application-level flooding attacks[[Ramkam-2006]](http://ieeexplore.ieee.org/xpl/login.jsp?tp=&arnumber=4146780&url=http%3A%2F%2Fieeexplore.ieee.org%2Fxpls%2Fabs_all.jsp%3Farnumber%3D4146780).

####  How (by using BotNet)
- Today, DDoS attacks are often launched by a network of remotely controlled, well organized, and widely scatterd Zombies or Botnet computers that are simulaneously and continuously sending a large amount of traffic and/or service requests to the target system. 
- Employing the resources of recruited computers to perform DDoS attacks allows attackers to launch a much larger and more disruptive attack.

#### BotNet, Zombies
- Attackers usually gain access to a large number of computer by exploiting their vulnerabilities to set up attack armies(i.e., Botnets). Once an attack army has been set up, an attacker can invoke a coordinated, large-scale attack against one or more targets. [[Zargar-2013]](../papers/ZargarJ13_Survey_Defense-Mechanism-against-DDoS.md)
- Zombies or computers that are part of a botnet are usually recruited throught the use of worm, Trojan horses or blackdoors.
