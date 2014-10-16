## [ViceROI: Catching Click-Spam in Search Ad Networks](http://dl.acm.org/citation.cfm?id=2516688)

- reading status: 10/16/2014 ing, finish Section 1,2
- bib
```
@inproceedings{Dave:2013:VCC:2508859.2516688,
 author = {Dave, Vacha and Guha, Saikat and Zhang, Yin},
 title = {ViceROI: Catching Click-spam in Search Ad Networks},
 booktitle = {Proceedings of The 20th ACM Conference on Computer and Communications Security(CCS)},
 year = {2013},
 pages = {765--776},
 numpages = {12}
} 
```

### Summary
In this paper, the authors proposed a principled approach to catching click-spam in search ad networks. It is designed based on the intuition that click-spam is a profit-making business that needs to deliver higher return on investment(ROI) for click-spammers than other (ethical) business models to offset the risk of getting caught.

### Strongness
- The designed mechanism is *proactive*. It makes no assumption on the attackers and could detect attacks without tuning parameters.
- Even if the mechanism is publicly disclose, it is not weakened, has advantage over *rule-based* mechanism(e.g., block by IP address)
- To avoid detection by ViceROI, the click-spammers must reduce their per-user revenue to that of an ethical publisher. At which point, without the economic incentive to offset the risk of being caught, the net effet is a disincentive to commit click-spam. 


### Weakness


### Learned
- Return-on-Investment(ROI)
	- As it is hard to estimate publisher ROI, so that they use per user revenue as a close approximate.

### Extension


### TODO
