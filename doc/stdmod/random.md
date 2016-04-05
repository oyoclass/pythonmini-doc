## random — Generate pseudo-random numbers
<!-- doc for this module is completed -->

This module implements a subset of Python standard ```random``` module, it contains pseudo-random number generators for various distributions. To use it, make sure use ```import random``` first.

### Functions

* ```random.choice(seq)``` : Return a random element from the non-empty sequence seq.
* ```random.randint(a, b)``` : Return a random integer N such that a <= N <= b
* ```random.random``` : Return the next random floating point number in the range [0.0, 1.0).
* ```random.randrange(stop)``` : See below.
* ```random.randrange(start, stop[, step])``` : Return a randomly selected element from *range(start, stop, step)*. This is equivalent to *choice(range(start, stop, step))*.
* ```random.seed(x)``` : Initialize the basic random number generator.
* ```random.shuffle(x)``` : Shuffle the sequence x in place.


### Example

```python
import random

lst = [1, 2, 3, 4, 5]

print random.choice(lst)

print random.randint(1, 10)

print random.random()

random.shuffle(lst)
print lst
```


### Reference

* [random module, python.org](https://docs.python.org/2/library/random.html)
