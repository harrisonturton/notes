# Circuits

### Adding

Modeling the addition function $$s(a,b)=a+b$$:

* If $$a$$ and $$b$$ are $$0$$, then the result is \(obviously\) $$0$$.

* If either $$a$$ or $$b$$ are $$1$$, then the result is $$1$$.

* If $$a$$ and $$b$$ are $$1$$, then the result is $$2$$.

Note that this does not work in binary -- we cannot have '2'. But if you consider addition in the 1s column, we can consider this a 'carry', i.e. the result is carried over to the next significant digit. Introduction another result, the _carry._

* If either $$a$$ or $$b$$ is** not** $$1$$, then the carry is $$0$$.
* If $$a$$ and $$b$$ are $$1$$, then the result is $$0$$ and the carry is $$1$$.



**Can be simplified to **$$s=a\oplus b$$ and $$c=a\wedge b$$.



