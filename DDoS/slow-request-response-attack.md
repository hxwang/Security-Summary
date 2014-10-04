2.4 Slow request/response attacks
----

In this type of attack, attackers send session that contain high-workload requests. There are a number of famous attacks in this category that we describe in the following.

###### 2.4.1 a Slowloris attack
- a.k.a, slow header attack
- Slowloris is a HTTP get-based attack that can bring down a Web server using a limited number of machines or even a single machine.
- The attacker send partical HTTP requests(not a complete set of request headers) that continuously and rapidly grow, slowly update, and never close.
- The attack continues until all available sockets are taken up by these requests and the Web server becomes inaccessible.
- Attacker' source addresses are usually not spoofed.

###### 2.4.2 HTTP fragementation attack
Similar to Slowlris, the goal of this attack is to bring down a web server by **holding up the HTTP connections for a long time without using raising any alarms**.
- Attackers (bots)(non-spoofed) establish a valid HTTP connection with a web server. Then they fragment legitimate HTTP packets into tiny fragments and send each fragment as slow as the server time out allows.
- Using this approach, by opening multiple sessions on each bot, the attacker can silently bring down a web server with just a handful of obts.


###### 2.4.3 Slowpost attack
Similar to Slowris, the attackers send HTTP post commands slowly to bring down web servers.
- The attacker sends a complete HTTP header that defines the *content-length* field of the post message body as it sends this request for benign traffic.
- Then it sends the data to fill the message body at a rate of one byte every two minutes.
- Hence, the serve waits for each message body to be completed while Slowpost attack grows rapidly which causes the DDoS flooding attack on the Web server.


###### 2.4.4 Slowreading attack
- This attack achieves its purpose by setting a smaller receive window-size than the target server's send buffer.
- The TCP protocol maintains open connections even if there is not data communications;
- Hence, the attackers can force the server to keep a large number of connections open and eventually causes the DDoS flooding attack on the server.