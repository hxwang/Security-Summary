## MTD Catagory based on Technical Type

- Ref
  - [Schmerl14](http://www.cs.cmu.edu/~garlan/publications/CMU-ISR-14-109.pdf)
    - Page 18, summary of various techniques and their impact on security and other quality measures

### N-Variant
- Tactics of this kind take advantage of the fact that the same functionaility in a system can be provided by multiple different implementations. 
- For example, in developing a web application, it is possible to use HTTP servers like Apache's Tomcat or Microsoft's IIS.
- N-Variant tactics have the feature where they can take advantages of both, either by fielding these variants simultaneously or by preiodically switching between them.
- From a defender's perspective, having multiple versions typically increases the cost of the system because multiple implementations must be developed and maintained, and may require additional resources at run time. It would be possible to alleviate this somewaht if variants could be automatically generated, for example, using different addresss randomization techniques multiple times and feilding these variants, described below, or by using genetic programming. 

### Randomization
- Many tactics tkae adavantage of various assumptions about the system to develop an exploit. 
- For example, SQL injection techniques take advantage of knowledge of SQL language and query conventions
- Rootkit take advantage of address layout and instructions sets to force jump into malicious code
- Randomization techniques such as RISE, HTML randomization and SQL randomization, attempt to avoid this by randomizing the instruction or languges.
- This makes it more difficult to inject attacks by writing, for example, standard SQL: if the SQL is not randomized in the same way as the system expects it will not compile as SQL. Furthermore, re-randomization can be done peroidically to invalidate any reconnaissaance that an attacker may have successfully performed.

### Refresh
- Refresh tactics attempt to return components to a known-safe state by either rebooting an existing component or by restoring a component to a previous checkpoint.

### Resource
- Resource tactics manipulate the resources that may be exploitable by either turning them off, setting limitations on how they may be used, or failing back to a safe set of components that are more thoroughly protected.
