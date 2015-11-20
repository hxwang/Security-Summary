## MTD Catagory based on Technical Type

- Ref
  - [Schmerl14](http://www.cs.cmu.edu/~garlan/publications/CMU-ISR-14-109.pdf)

### N-Variant
- Tactics of this kind take advantage of the fact that the same functionaility in a system can be provided by multiple different implementations. 
- For example, in developing a web application, it is possible to use HTTP servers like Apache's Tomcat or Microsoft's IIS.
- N-Variant tactics have the feature where they can take advantages of both, either by fielding these variants simultaneously or by preiodically switching between them.
- From a defender's perspective, having multiple versions typically increases the cost of the system because multiple implementations must be developed and maintained, and may require additional resources at run time. It would be possible to alleviate this somewaht if variants could be automatically generated, for example, using different addresss randomization techniques multiple times and feilding these variants, described below, or by using genetic programming. 
