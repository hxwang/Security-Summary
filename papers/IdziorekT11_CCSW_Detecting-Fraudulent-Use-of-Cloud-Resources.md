[Detecting Fraudulent Use of Cloud Resources](http://dl.acm.org/citation.cfm?id=2046676)
---

- reading status: finished on 10/13/2014
- bib
```
@inproceedings{IdziorekT11,
    author = {Idziorek, Joseph and Tannian, Mark and Jacobson, Doug},
    title = {Detecting Fraudulent Use of Cloud Resources},
    booktitle = {Proceedings of the 3rd ACM Workshop on Cloud Computing Security Workshop(CCSW)},
    year = {2011},
    pages = {61--72},
    numpages = {12}
} 
```

### Summary
In this paper, the authors first point out that the traditional mechanism for detecting DDoS attack cannot be applied to detect FRC attack. Then they proposed three detection metrics form the criteria for identifying a FRC attack from that of normal web activity. Evaluations are conducted under three make-up attack scenarios. 

### Model
- System Model
The following rles are defined in the context of cloud computing to provide a consistent reference to the actors that play in a FRC attack.
    - *Cloud Service Provider(CSP)**
      - The CSP(e.g., Amazon EC2 or Microsoft Azure) offers consumer-provisioned and metered computing resources that can be leased for flexible time durations.
    - *Cloud Consumer*
        - The cloud consumer is a person or organization that employs the services of a CSP and is financially responsible for resource consumption. 
        - The cloud consumer also plays a dual role of the victim.
    - *Client*
        - The client is a legitimate user that requests web content offered by the cloud consumer.
    - *Attacker*
        - Although a FRC attack is ultimately carried by one or more attack clients, the attackers(e.g., bot master) is the mastermined that orchestrates the FRC among the attack clients. 
    - *Attack Client*
        - The attack client is a malicious user(e.g., bot) that fraudulently consumes resources offered by the cloud consumer. 
- Utility Model
    - [Pay-As-You-Go](../Cloud/file/pricing.md)
    
### DDoS v.s. Flash Crowd
- Definition
    - Flash crowd: a significnat number of legitimae clients simultaneously requesting web content from a given site. Often triggered by a major news or sporting event, the individual clients that participate in this phenomenon are not malicious in nature.
- Similarity
    - traffic peak
- Difference
    - in DDoS attack, the average client request is high during the peak
    - in Flash Crowd, the average client request rate will decrease due to the decrease of QoS quality
- In the following figure, it shows a graph of request per second for a week-long web trace from a busy NASA web server [[NASA-Trace]](ftp://ita.ee.lbl.gov/html/contrib/NASA-HTTP.html)
    <div align = "center">
        <img src= "../figs/DDoS-Flash-Crowd.PNG" width = "800px" />
    </div>

### Detection Metrics

- Metrics1: based on Zip law
The proposed metrics are based on the consistency and self-similar nature of aggregate web activity.
    - Observation
        - In the normal case, the document request will satisfy Zip law.
        - However, for the FRC attack, attackers will have more interest in requesting for the documents that represent the majority of overall data usage. 
    - How it works?
        - computing the 90% regression slop of a sample data set
        - determine if the slope falls within a tolerance interval relative to normal activity
    - Resiliency
        - if the attacker want to avoid being detected, then the attackers to know the website's usage patterns
- Metric2: based on Spearman's Footrule
Detect the presence of resource usage fraud within an inspected dataset(i.e., the ground truth is known)
    - intro
        - The Spearman's Footrule distance [[Dwork-2001]](http://dl.acm.org/citation.cfm?id=372165) is a non-parametric measure of **similarity**, or lack thereof, between two ranked lists.
        - the greater the Spearman proximity between two top_k ranked lists, the more similar the two lists are in respect to each other.
- Metric3: overlap
        
### Evaluation
- attack scenario
    - the authors describe three attack scenarios: random attack, heavy-hitter attack and trace-drive attack.
    - the evaluation is performed under these three attack scenarios 
- evaluation metrics
    - false positive
    - false negative
    



### Extensions
- Although the detection mechanism present in this paper can detect FRC attack, it is not capable of identifying of individual attack clients from legitimate clients
    - However, our shuffling mechanism can! How to map our mechanism to solve the problem?
    

### TODO
- page 65: archive the related work on detection mechanism in this paper 
