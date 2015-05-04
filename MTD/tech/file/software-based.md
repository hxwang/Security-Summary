## Software-based Diversification

- [ref](http://dl.acm.org/citation.cfm?id=2663486)

Existing works achieve Software-based Diversificiation via directly manipulating software or replying on compilers to produce diversification.

### Software Manipulation
- The technqiue of software manipulation enchances security via changing software functionality to eliminate vulnerabilities or limit their exposure. 
- Accretion, excision, and replacement of funtionality are all leveraged as manipulation mechanisms.
- Input rectification is an example ofa accretion mechanism.
- Via insrting functions to manipulate inputs in software, input rectification converts each input to stay in secure zone. For instance, the Pine email rectifier is developed to force messages into a specific constrained form. In order to simplify software behavior and possibly avoid vulnerabilities, functionality excision removes functional but non-critical sections of a program, which may introduce result noise, but normally will not cause failure. 
- Functionality replacement switches between different implementations of the same function in a program, and thus generate system variation to neutralize attacks.

### Compiler-generated Diversity 
There are two types of compier-based diversity technqiues: Malt-Variant Execution Environment (MVEE) and Massive-Scale Software Diversity (MSSD). Both of them rely on automated tools, especially the compiler, to produce functionally equivalment, but internally different program variants.
- Within MVEE, multiple semantically equivalment variant of a program are executed, and their behaviors are compared at synchronization points. Diverging behavior detected during synchronization indicates potential attacks.
- As early as in the 1970s, Chen and Avizenis developed a technique known as N-Version Programming, to generate N >=2 functionsally equivalment programs. The mechanism required to achieve N-Version programming could be completed by a compiler.
- The SQL interpreter known as SQLrand, prevents SQL injection by randomizaing the standard Query Language, and relflects the idea of MVEE.
- MSSD refers to the idea of relasing divesified software variants to each user, and thus hides the internal struture of software variants from attackers. Code Sequence Randomization (CSR) is a MSSD technqiue that users intsruction schemeling, call inlining, code hoisting, loop distribution, partical redundancy elminication, and many other compler transofmraitons to generate variants of machine codes. CSR could mitigate attacks thay rely on knowledge about instracution at certain locations, such as return oriented programming attack. Equivalment Instruction (EI) is another MSSD technique. In software, EI stands for a set of instruction sequences that have identical effects and can be substituted for one another. Variants of machine code could be produced by replacing instructions through EI.
