1. Explain Python GIL
Technically, GIL is a lock of the interpreter that any execution of python bytecode needs to acquire.

* SO answer:
https://stackoverflow.com/questions/1294382/what-is-the-global-interpreter-lock-gil-in-cpython

1. What is Understore _ 
https://hackernoon.com/understanding-the-underscore-of-python-309d1a029edc


1. In Python, what is the difference between a generator  expression and a list comprehension?
Generator evaluates a next on call, list evaluates and stores all results in one shot.

For example,
Example of list comprehension: [x*2 for x in range(10) if x%2]
Example of generator expression: (x*2 for x in range(10) if x%2)

Notes: In Python 3.7, range is implemented as lazy generator, so no more xrange
