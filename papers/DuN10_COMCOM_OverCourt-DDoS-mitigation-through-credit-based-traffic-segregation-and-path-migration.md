[OverCourt: DDoS Mitigation through credit-based traffic segration and path mitigation](http://www.sciencedirect.com/science/article/pii/S0140366410004251)
---

- reading status: haven't started
- bib
```
@article{Du20102164,
    title = "OverCourt: \{DDoS\} mitigation through credit-based traffic segregation and path migration ",
    author = "Ping Du and Akihiro Nakao",
    journal = "Computer Communications ",
    volume = "33",
    number = "18",
    pages = "2164 - 2175",
    year = "2010"
}
```

### Summary
- In this paper, they propose an **overlay-based** DDoS mitigation architecture by introducing a **credit-based** accounting mechanism.

### Model
- Architecture (OverCourt)
    - Two classes of communication channel
        - VIP(very important person)
        - non-VIP 
    - The architecture is shown in the following figure.
    ![](https://github.com/hxwang/Security-Summary/blob/master/figs/OverCourt-arch.PNG = 250x)
    
- Migrate
    - A well-behaving client may dynamically migrate to a protected channel when her credit points exceed a threshold while an ill-behaving client will be blocked after her credit points have been exhausted. 
    - Technical: since a pth is established through a tunnel(virtual link), so we can migrate the traffic path of a well-behaving client from a non-VIP channel to a protected VIP channel

- Mechanism
    - clients with different credit points are served on different communication channels. 
    - a sender can send packets based on her credit points earned by her legitimate communication behaviors instead of expending resources in advance.
        - since the credit points given to a sender is designed to be measured based on her history of communication patterns, a well-behaving sender can gain her credit points while an ill-behaving one will lose her credit points. 
    

### Strongness

### Weakness

### Extension
