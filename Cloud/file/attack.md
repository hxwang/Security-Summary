## Cloud Attack

### 1. Fradulent Resource Consumption(FRC) attack
Ref: [[Idziorek-2011]](../../papers/IdziorekT11_CCSW_Detecting-Fraudulent-Use-of-Cloud-Resources.md)
##### Attack Objective
- The objective of the attacker is to exploit the utility pricing model by fraudulently consuming web content with the purpose of depriving the victim of their long-term economic viability of hosting publicly accessible web content in the cloud.
  - under the **pay-as-you-go scheme**, attackers intend to run-up the data usage cost for the victime by consuming bandwidth in excess of normal usage.
  - Cloud network attack diagram
    - <img src="../figs/CloudEdosAttack.PNG" width="550px" />
    
#### Attacker Characteristic
- to avoid detection by current application-layer DDoS solutions, fraudulent request rates of attack clients are of **moderate intensity** and requests attempt to lend into the normal activity of the target website. 

#### Detection
- For the cloud consumer, differentiating data usage of legitimate clients from that of attack clients is difficult because requests only differ in the intentions of the attacker not in the structure or semantics of the requests/ 
