## EDoS Defense Mechanism

### Turing Tests
- Turing Tests [[Ahn-2004]](http://dl.acm.org/citation.cfm?id=966390) can be used to differentiate humans and attack clients.
- Drawbacks
    - Turing tests have been found to be unreliable and have been circumvented by mechanical Turks [[Bursztein-2010]](http://dl.acm.org/citation.cfm?id=1849987) and puzzle breaking schemes [[Yan-2008]](http://dl.acm.org/citation.cfm?id=1455839)
    - Moreover, requiring a casual web users to solve a graphical puzzle to simply view is counter to the goals of the web application as some users are unable or simply unwilling to deal with the hassle [[Oikonomou-2009]](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=5199191&tag=1) [[Ranjan-2009]](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=4555692)
    
### CloudWatch
- [CloudWatch](http://aws.amazon.com/cloudwatch/) is an auto scaling techniqu enabled by Amazon as a control technology that will reduce the effects of the EDoS attacks.  CloudWatch is a web service that provides monitoring for cloud resources by which clients will be able to define *boundaries* that would limit the elasticity of their cloud platforms and thus reducing the effect of the EDoS attacks. 
- Drawback
    - however, this cannot be considered as an efficient practical solution for the EDoS attack since the user account could still be charged to some extent defined by quota due to such attack. In addition, when elasticity reaches the upper bound, the cloud service freezes and thus legitimate clients will be denied service till refreshing the quota again leading to a behavior similar to a DoS attack.

### sPoW
- sPoW [[]HinkhorN-2009]](http://www.docstoc.com/docs/104260160/sPoW-On-Demand-Cloud-based-eDDoS-Mitigation-Mechanism) 
- my comment: `the idea is similar to turing test`

### CLAD
- Ref: [[PingN-2010]](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=5488345)
- CLAD is a cloud-based **overlay** network, which is an on-demand network service to proect the web-servers against the DDoS. 
- how it works?
    - mediates the traffic targeting the protected server to verity the clients using graphical Truing tests.
- Pros
    - implementing the overlay network in the cloud infrastructure is a promising idea since the cloud has an aggregated capacity exceeding that of most of the botnets. 
- Cons
    - increase the end to end latency [[Beitollahi-2008]](http://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=4536157) due to indirection where the overlay network mediates all the traffic between the clients and the target server.
    
    
    
