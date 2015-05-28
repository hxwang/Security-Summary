## [A Model for Analyzing the Effect of Moving Target Defenses on Enterprise Networks](http://dl.acm.org/citation.cfm?id=2602088)

### Summary
In this paper, the authors model the moving target defense problem by consider a simple network graph. The motivation is to provide insight of configuring defense strength to guarantee security (measured by attacking likelihood). Part of the contents is suammrized [here](../../model)

### Highlight
- Adaption Interval: the time interval between each system adaption. 
  - If a node does not get adaption during the attack interval, it will have probability to be attacked.
  
### Questions
- The calculation of p2, p3, p4, p5 is different from my derivation.
- Why in the experiments, the theoretical attack sucessful probability is higher than the experiments?
  - As in the theoretical model, the back transition is eliminated, thus the theoretical value is assumed to be lower. As the attackers in an adapted node will be eliminated, and will not be backward transition to the predecessor of this adapted node.

### TODO
- Do simulation. Check the corretness of my derivation.
