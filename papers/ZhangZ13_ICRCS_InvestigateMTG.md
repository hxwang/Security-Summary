## [Investigating the Application of Moving Target Defenses to Network Security](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=6623770)

- reading status: finished on 10/17/2014
- bib
```
@INPROCEEDINGS{ZhangZ13, 
  author={Rui Zhuang and Su Zhang and Bardas, A. and DeLoach, S.A. and Xinming Ou and Singhal, A.}, 
  booktitle={The 6th International Symposium onResilient Control Systems (ISRCS)}, 
  title={Investigating the application of moving target defenses to network security}, 
  year={2013}, 
  pages={162-169}
}
```


### Summary
In this paper, the author study the effects of randomly adapting one aspect of the system(role to VM mapping) in reducing attacker's sucess likelihood. 

### Strongness
- design simulation to study the effectiveness of moving target defense

### Weakness
- only experiment study, no theoretical model and analysis

### Learned 
- Simulation
  - They define adaption interval of the defender, which is the react time for the defender to refresh from attack. And then they show simulation result under different adaption interval. 

### TODO
- I didn't investigate the detail of "refresh VM". In my view, when the attackers attack a VM,the defender could simply refresh the VM to recover from the attack. I am not sure. Although this point is not important for now, in the future, if I examine the paper again, I will pay attention to this issue.


### Extension

