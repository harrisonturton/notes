# Design Patterns

A design pattern is a good solution to a recurring problem in software design.  
A single design may be compromised of multiple design patterns.

**Advantages:**

* Capture expert design knowledge and make it accessible in a standardized way
* Promotes communications & streamlines documentation by providing shorthands
* Supports software reuse and increases software quality and designer productivity
* Provides a model to be improved upon

**Disadvantages:**

* Can over-complicate a design
* Some patterns are difficult to understand
* Can be difficult to implement in a certain language \(concepts are language-agnostic\)
* May adversely affect time/space performance.

Need to be mindful of:

* Where information is held in the design
* How different parts relate to eachother
* How requirements are likely to change over time

**Designing to an interface provides enormous flexibility as code changes.**

### Model-View-Controller Design Pattern

Often used for GUI development. Separates GUI design into three parts.

**Model  
**Stores information. Does not include _any _functionality about how data is viewed or changed/updated.

**View  
**Provides a way to view data that is stored in the model, and ways to interact with the controller.

**Controller  
**Provides code that allows the user to control or change data in the model.





