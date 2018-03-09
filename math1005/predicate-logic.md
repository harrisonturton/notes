### Predicates

**Predicate: **A sentence that becomes a statement when values are given to it's variables, e.g: $$P(x)\implies x\text{ is a bird}$$.

**Domain: **The domain of a predicate is the set of values the variables can take.

$$P(x)\implies x\text{ can view this file. Domain: Users}$$

$$G(x)\implies x^2+2=3 \text{ Domain: Numbers}$$

### Quantifiers

A predicate can be turned into a statement by either:

* Giving the variables values
* Quantifying the values \(binding to arbitrary values\)

| Quantifier | Symbol | Meaning |
| :--- | :--- | :--- |
| Universal Quantifier | $$\forall x$$ | Every $$x$$ ... \(Could be none\)$$$$ |
| Existential Quantifier | $$\exists x$$ | There is **at least one **$$x$$ that ... |
| Unique Existential Quantifier | $$!\exists x$$ | There is a **unique **$$x$$ that ... |

#### Negating Quantified Statements

To negate a statement, you must negate the equality, the quantifiers, and the logical connectives.

| Quantifier | Negation |
| :--- | :--- |
| $$\wedge$$ AND | $$\vee$$ OR |
| $$=$$ EQUALS | $$\neq$$ NOT EQUALS |
| $$\forall$$ FORALL | $$\exists$$ THERE EXISTS |
| $$!\exists$$ THERE EXISTS UNIQUE | $$\forall x(\neg P(x) \wedge \exists y(x\neq y \wedge P(x))$$ i.e. There is no value for which the predicate doesn't hold, and there are at least two non-equal arbitrary values where the predicate does hold. |



