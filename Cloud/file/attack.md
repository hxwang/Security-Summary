## Cloud Attack

### Fradulent Resource Consumption(FRC) attack
Ref: [[Idziorek-2011]](../../papers/IdziorekT11_CCSW_Detecting-Fraudulent-Use-of-Cloud-Resources.md)
##### Attack Objective
- The objective of the attacke ris to exploit the utility pricing model by fradumlently consuming web content with the purpose of depriving the victime of their long-term economic viability of hosting publicly accessible web content in the cloud.
  - under the **pay-as-you-go scheme**, attackers could attack the economic sustainability of cloud consumers, i.e., the attackers could request web content in volumes that cost the cloud consumer a lot of money
  - Cloud network attack diagram
    - <img src="../figs/CloudEdosAttack.PNG" width="550px" />
    
#### Attacker Characteristic
- to avoid detection by current application-layer DDoS solutions, fraudulent request rates of attack clients are of **moderate itensity** and requests attempt to lend into the normal activity of the target website. 

#### Detection
- For the cloud consumer, differentiating data usage of legitimate clients from that of attack clients is difficult because requests only differe in the intentions of the attacker not in the structure or semantics of the requests/ 
