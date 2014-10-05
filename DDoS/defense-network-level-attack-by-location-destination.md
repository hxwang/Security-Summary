Defense mechanisms against network/transport-level DDoS attacks(destination based mechanisms)
---

- Note: contents of this page are from paper [Zigzag-2013]()

- In the destination-base defense mechanisms, detection and response is mostly done at the destination of the attack(i.e., the victim). There exist various destination-based mechanisms that can take place either at the edge routers or the access routers of the destinations' AS. These mechanisms can closely observe the victim, model its behavior and detect anomalies. Some ofthe major destination-based DDoS defense mechanisms are as follows.

#### IP Trackback Mechanisms
- Ref: [[John-2009]](http://academypublisher.com/ijrte/vol01/no02/ijrte0102241245.pdf) 
- How it works?
	- The process of tracing back the forged IP packets to their sources rather than the spoofed IP addressed that was used in the attack is called traceback.
	
	
- Categories
There are various IP traceback mechanisms that have been proposed to date [[Chen-2006]](http://ieeexplore.ieee.org/xpl/login.jsp?tp=&arnumber=4150942&url=http%3A%2F%2Fieeexplore.ieee.org%2Fxpls%2Fabs_all.jsp%3Farnumber%3D4150942). These mechanisms can be classified into two categories.
	- 1. Packet marking mechanisms
		- [[Chen-2006]](http://ieeexplore.ieee.org/xpl/login.jsp?tp=&arnumber=4150942&url=http%3A%2F%2Fieeexplore.ieee.org%2Fxpls%2Fabs_all.jsp%3Farnumber%3D4150942)
		[[Duwairi-2006]](http://dl.acm.org/citation.cfm?id=1130864)
		[[Savage-2000]](http://dl.acm.org/citation.cfm?id=347560)
		- How it works
			- Usually routers in the path to the victim mark the packets (i.e., add routers' identification to each packet) so that the victim can identify the path of attack traffic and distinguish it from legitimate traffic after the detection. 
		- Drawback
			- However, storing the entire path in the IP identification field of each packet needs certain coding schemes and these schemes sometimes are not able to assign each mark to a unique path; hence, false positive rates of these mechanisms are still high. In other words, legitimate packets can be treated as attack packets.
	- 2. Link testing mechanisms
		- Ref: [[Burch-2000]](https://www.usenix.org/legacy/publications/library/proceedings/lisa2000/full_papers/burch/burch_html/index.html)
		[[Glave-1998]](http://archive.wired.com/science/discoveries/news/1998/01/9506)
		- How it works
			- The trace process usually starts from the router closest to the victim and iteratively tests its upstream links until it can determined which link is used to carry the attackers' traffic. (i.e., the traceback process is **recursively repeated** on the upstream router until the source is reached).
	
- Drawback
	- All of the traceback mechanisms have serious deployment and operational challenges [[Wu-2011]](http://ieeexplore.ieee.org/xpl/login.jsp?tp=&arnumber=5318904&url=http%3A%2F%2Fieeexplore.ieee.org%2Fxpls%2Fabs_all.jsp%3Farnumber%3D5318904). 
	- One of the fundamental deployment and operational challenges is ensuring a sufficient number of routers that support traceback before it is effective.
	- Moreover, attackers can also aggregate generate traceback messages; consequently, some form of authentication of traceback message is necessary.
	- Furthermore, most of the traceback mechanisms have heavy computational, network or management overheads [[Wu-2011]](http://ieeexplore.ieee.org/xpl/login.jsp?tp=&arnumber=5318904&url=http%3A%2F%2Fieeexplore.ieee.org%2Fxpls%2Fabs_all.jsp%3Farnumber%3D5318904).


#### Management Information Base(MIB)
- Ref: [


#### TODO
- [ ] Read page 2054-2055 of [Zigzag-2013]()