# Software Design

Idea &gt; Implementation &gt; Interaction

### Good Design

It is easy to overcomplicate design & make it difficult to add extra functionality.

Good design can be defined as creating:

* Robust
* Maintainable
* Flexible

### Top-Down Design

* Keep dividing main problem into sub-problems until each problem can be solved.
* Once each sub-problem is solved, they accumulate to solve bigger problems.
* **Often produces BAD OO design**
* When sub-dividing a problem, think **in terms of Data, not the process.**

### Bottom-Up Design

Considers the modules already provided & how they can be composed to form a solution

When we think of OO design, the import things are:

* Data that needs representation
* Relationship between different data elements
* Libraries that need to be used & how they are normally interfaced

### Software Quality Metrics

In terms of _design, _there are three important metrics:

1. **Coupling **- Bad. How connected different modules are. Minimise.
2. **Cohesion **- Good. How closely different parts/functions within a single are related. Maximise.
3. **Open/Closed** - The principle that code should be _open _for extension yet _closed _for modification.

### Classes & Interfaces

**Classes:**

* Hold data
* Define relationships between data
* Provide methods to interact with data

Each class should focus on one main aspect. Use Nouns for classes.

**Interfaces:**

* Provide a flexible way for code to interact
* Help reduce coupling
* Provide the ability to change or replace modules of code.

### Design Tips

* Use an iterative approach
  * Expect to refactor and redesign your code
* Look for patterns that repeat. Consider how these can be reduced, and if there is a better design approach.
* Look for 'library' type code. Seperate it, and generalise it beyond this program.





 





