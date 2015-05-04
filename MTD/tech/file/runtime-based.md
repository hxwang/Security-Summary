## Runtime-based Diversificaiton

- [ref](http://dl.acm.org/citation.cfm?id=2663486)

Many defenses techniques mitigate attacks via introducing diversificaiton in runtime environments. 
- Address Space Layout Randomization (ASLR) is a widely known example of Runtime-based Diversification techniques. 
  - ASLR randomly arranges tarting positions of key code and data areas in a process's address space, including the base memeory address of the executable, the stack, the heap, and the libaries, to prevent an attack from corretly jumping to a particular exploited function in memory.
  - Kc et al. present an Instruction Set Randomization (ISR) algorithm based MVEE techqniue. With ISR, operatos in machine isntrucitons are encoded with a randomization key during compilation. Immediately before execution, operators in randomized instricutions are required to be correctly decoded. 
  - In a program instance with ISR, code injected by attackers will not perperly ecoded but still go though the decoding process. This lead to illegal CPU instructions and exceptions, or at least different execution resutls from the program instance without ISR. 
  - Instead of encoding instruction, SCNR encodes system calls in a program. With SCNR, execution of injected code that contains incorrectly encoded ystem call leads to an error, or a differentresult from the normal program.
