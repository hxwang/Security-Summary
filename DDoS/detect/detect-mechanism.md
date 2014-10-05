## DDoS detection mechanism

There exist multiple detection schemes

#### Abnormal traffic volume
- Ref: [[Dainotti-2006]](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=4150909)
[[Brutlag-2002]](http://dl.acm.org/citation.cfm?id=1045530)
[[Cheng-2002]](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=1189011)
- They propose attack detection through analyzing abrupt changes in the time series of traffic volume.
 
#### Abnormal packet size
- Ref:  [[Du-2007]](http://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=4610090)
- They detect based on the abnormal packet size distribution

#### Graphic Turing Test
- [[Kandula-2005]](https://www.usenix.org/legacy/event/nsdi05/tech/kandula/kandula.pdf)

#### Attack pattern
- Bro[[Paxson-1998]](http://dl.acm.org/citation.cfm?id=337972) , Snort [[Roesch-1999]](http://dl.acm.org/citation.cfm?id=1039834.1039864)
 
#### Two way traffic rates
- [MULTOPS](http://www.utdallas.edu/~kxs028100/Papers/multops.pdf) and [D-WARD](http://www.isi.edu/~mirkovic/publications/nca03.pdf) 