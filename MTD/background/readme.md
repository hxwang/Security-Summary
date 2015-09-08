## Background


### Attacks
- **Convert channel** [[Wang]](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.190.1003&rep=rep1&type=pdf)
  - A convert channel users mechanisms that are not intended for communications, .e.g, writting and checking if a file is locked to convey a "1" or "0". In convert channel, an insider process leaks information to an outsider process not normally allowed to access that information. 
  - The insider (sending) process could be a Trojan horse program previously inserted stealthily into the computer.
  - An outsider (receiving) process need only to be an unpriviledged process.
- **Side channel** [[Wang]](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.190.1003&rep=rep1&type=pdf)
  - In a physical side channel attack, unconventional techniques are used to deduce secret information. 
  - Typically, the device has physical access to it for launching a physical side-channel attack. 
  - Traditional side channel attacks involved differential power analysis and timing analysis. Different amount of powr (or time) used by the device in performancing an encruption can be measured and analyzed to deduce some or all of the key bits.
