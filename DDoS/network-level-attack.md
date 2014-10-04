Network/transport-level DDoS flooding attacks
---

These attacks have been mostly launched using TCP, UDP, ICMP and DNS protocol packets.There are for types of attacks in this category [[Mirkovic-2006]](http://dl.acm.org/citation.cfm?id=997156),[[Douligeris-2004]](http://www.sciencedirect.com/science/article/pii/S1389128603004250).

#### Flooding attacks
- Attackers focus on disrupting legitimate user's connectivity by exhausting victim network's bandwidth (e.g., Spoofed/non-spoofed UDP flood, ICMP flood, DNS flood, VoIP flood and etc [[Pend-2004]](http://dl.acm.org/citation.cfm?id=1216373) [[RioRey-2012]](https://www.scribd.com/doc/92863121/RioRey-Taxonomy-DDoS-Attacks-2-2-2011) ).


#### Protocol exploitation flooding attacks
- Attackers exploit specific fetures or implementation bugs of some of victim's protocols in order to consume excess amounts of the victim's resources (e.g., TCP SYN flood, TCP SYN-ACK flood, ACK & PUSH ACK flood, RST/FIN flood and etc [[Pend-2004]](http://dl.acm.org/citation.cfm?id=1216373) [[RioRey-2012]](https://www.scribd.com/doc/92863121/RioRey-Taxonomy-DDoS-Attacks-2-2-2011) ). 

#### Reflection-based flooding attacks
- Attackers usually send forged requests( e.g. ICMP echo request) instead of direct requests to the reflectors; hence, those reflectors send their replies to the victim and exhaust victim's resources (e.g., Smurf and Fraggle attacks [[Pend-2004]](http://dl.acm.org/citation.cfm?id=1216373),[[Douligeris-2004]](http://www.sciencedirect.com/science/article/pii/S1389128603004250).

#### Amplification-based flooding attacks
- Attackers exploit services to generate large messages or multiple messages for each message they receive to amplify the traffic towards the victim.
- Botnets have been constantly used for both reflection and amplification purposes. Reflection and amplification techniques are usually employed in tandem as in the case of Smurf attack where attackers send requests with spoofed source IP addresses(Reflection) to a large number of reflectors by exploiting IP broadcast feature of the packets [[Pend-2004]](http://dl.acm.org/citation.cfm?id=1216373),[[Douligeris-2004]](http://www.sciencedirect.com/science/article/pii/S1389128603004250).



#### TODO
- [ ] Add more details explanation of these attacks.