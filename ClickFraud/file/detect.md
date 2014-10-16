## Click Fraud Detection

Detecting click fraud is conceptually challenging tasks. We can classify invalid click-detection methods under three categories [[Kshetri-2010]](../papers/Kshetri10_The-economics-of-click-fraud.md), i.e., *Anomaly-based*, *Rule-based* and *Classifier-based*.

### Anomaly-based 
or **deviation-from-norm-based**
- how it works?
    - consider **invalid clicks** to be those that deviate significantly from normal predicted behaviors.
    - involve analyzing offline aggregate data related to day-to-day activities to capture **normal behaviors** and derive a model.
    - instead of defining an invalid click, this approach defines a normal click and determines whether other clicks vary widely from the normal one
- challenge
    - determine what comprises normal and how much deviation is significant
    
### Rule-based 
- how it works?
    - use heuristics to classify valid and invalid clicks on the basis of specific conditions
        - e.g., if two successive clicks occur, the second click might be an invalid one
        - PPC providers can implement **session tracking** to track a series of requests from the same user across a given period
        
### Classifier-based
- how it works
    - employ data mining classifier labels to detect invalid clicks
    - base on the assumption that past clicking behavior predict future clicking behavior
- challenge
    - it assumes the advisers has past data, which classifiers a click as valid or invalid with certain level of confidence and doesn't consider the properties of valid or invalid clicks discussed in the previous approaches.


---
### Detection accuracy
- A controlled measurement study conducted in 2012 found that major ad networks still missed ongoing click-spam attacks that accounted for an estimated 10-25% of clicks in the study [[DaveG12]](http://dl.acm.org/citation.cfm?id=2377715)