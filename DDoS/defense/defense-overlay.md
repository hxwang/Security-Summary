## Overlay Defense Mechanism


### SOS
- [[Kermytis-2002]](http://www.cs.columbia.edu/~angelos/Papers/sos.pdf) SOS is the first idea of using an overlay network to provide DDoS defense. The goal of SOS infrastructure is to distinguish between authorized and unauthorized traffic, where the former is allowed to enter the destination and the latter is dropped.

### Mayday
- [[Anderson-2003]](http://www.cs.cmu.edu/~dga/papers/mayday-usits2003/) Mayday generalizes SOS by separating routing and filtering mechanism, which discusses tradeoff between security and performance. 

### WebSOS, MOVE
- [[Cook-2003]](http://www.cs.columbia.edu/~angelos/Papers/websos-icon.pdf)  WebSOS
- [[Stavrou]](http://www.cs.columbia.edu/~angelos/Papers/2005/move-ndss.pdf)  MOVE
- Both of these use graphical Turing tests to differentiate human users from attack zombies, instead of public-key in the original SOS, to authenticate the clietns accessing the web server.
