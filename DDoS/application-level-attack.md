## Application-level DDoS flooding attacks
---
* Most contents in this page is from paper [[Zargar]]()


- These attacks focus on disrupting legitimate user's services by exhausting the server resources (e.g., Sockets, CPU, memory, disk/databased bandwidth, and I/O bandwidth) [[Ranjan-2006]](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=4146780&tag=1)
- Application-level DDoS attacks generally consume less bandwidth and are stealthier in nature compared to volumetric attacks since **they are very similar to benign traffic**. 
- However, application-level DDoS flooding attacks usually have the same impact to the services since they target specific characteristics of applications such as HTTP. DNS, or Session Initiation Protocol(SIP).

#### 1. Reflection/amplification based flooding attacks
- [[Pend-2004]](http://dl.acm.org/citation.cfm?id=1216373),[[Douligeris-2004]](http://www.sciencedirect.com/science/article/pii/S1389128603004250).
- These attacks use the same techniques as their network/tranport-level peers (i.e., sending forged application-level protocol requests to the large number of reflectors). 
- For instance, the DNS amplification attack employs both reflection and amplification techniques. 
    - The attackers(zombies) generate **small** DNS queries with forged source IP addresses which can generate a **large** volume of network traffic since DNS response messages may be substantially larger than DNS query messages. 
    - Then this large volume of network traffic is directed towards the targeted system to paralyze it.
- Another example is VoIP flooding.
    - This attack is a variance of an application specific UDP flooding. 
    - Attackers usually send spoofed VoIP packets through SIP at a very high packet rate and with a very large source IP range. 
    - The victim VoIP server ha to distinguish the proper VoIP connections from the forged ones that consume significant amount of resources.
    - VoIP flooding can overwhelm a network with packets with randomized or fixed source IP addresses. If the source IP address has not been changed the VoIP flooding mimics traffic from large VoIP servers and can  be very difficult to identify since it resembles good traffic.

#### 2. HTTP flooding attacks
There are four types of attacks in this category.

##### 2.1 Session flooding attacks
- In this type of attack, session connection request rates from the attackers are higher than the requests from the legitimate users. Hence, this **exhausts the server resources** and leads to DDoS flooding attack on the server
- One of the famous attack in this category is the **HTTP get/post flooding attack**, (a.k.a., excessive VERB)  
    - Attackers generate a large number of valid HTTP (get/post) to a victim web server
    - Attackers often employ botnets to launch these attacks, since each of the bots can generate a large number of valid requests(usually more than **10 requests a second**) there is no need for a large number of bots to launch a successful attack. 
    - HTTP get/post flooding attacks are **non-spoofed** attacks.
    
##### 2.2 Request flooding attacks
- In this type of attack, attackers send sessions that contain more number of requests than usual and leads to a DDoS flooding attack on the server
- One of the well know attacks in this category is the **single-session HTTP get/post flooding** (a.k.a., excessive VERB single session)
    - this attack is a variation of HTTP get/post flooding attack which employs the feature of HTTP 1.1 to allow multiple requests within a single HTTP session.
    - Hence the attack can limit the session rate of an HTTP attack and bypass session rate limitation defense mechanisms of many security systems.
    
##### 2.3 Asymmetric attacks
In this type of attack, attackers send sessions that contain **high-workload requests**. Here, we enumerate some of the famous attacks in this category.
###### 2.3.1 Multiple HTTP get/post flood
- This attack is also a variation of HTTP get/post flood attack
- Here, an attacker creates multiple HTTP requests by **forming a single packet embeded with multiple requests** and without issuing them one after another within a single HTTP session.
- This way attacker can still maintain high loads on the victim server with a low attack packet rate which makes the attacker nearly invisible to netflow anomaly detection techniques. 
- Also, attackers can easily bypass deep packet inspection techniques if they carefully select the HTTP VERB.
    
###### 2.3.2 Faulty Application
- In this attack, attackers take advantage of websites with poor design or improper integration with databases.
- For instance, they can employ SQL-like injections to generate requests to lock up database queries. These attacks are highly specific and effective because they consume server resources (memory, CPU etc.)
    
##### 2.4 Slow request/response attacks

In this type of attack, attackers send session that contain high-workload requests. There are a number of famous attacks in this category that we describe in the [Ref](https://github.com/hxwang/Security-Summary/blob/master/DDoS/slow-request-response-attack.md).

###### 2.4.1 a Slowloris attack
###### 2.4.2 HTTP fragementation attack
###### 2.4.3 Slowpost attack
###### 2.4.4 Slowreading attack









#### Thoughts
- `maybe we can target our moving target model to combat the application-level ddos attack. Since this assumption is in favor of our mechanism that attackers are hard to be distinguish from the benign clients by traffic. Also, we can simulate small number of insiders. `
