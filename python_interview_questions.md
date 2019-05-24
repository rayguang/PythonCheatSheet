### Explain Python GIL
Technically, GIL is a lock of the interpreter that any execution of python bytecode needs to acquire.

* SO answer:
https://stackoverflow.com/questions/1294382/what-is-the-global-interpreter-lock-gil-in-cpython

### Explain Python data structure
* list: ordered, non-unique, mutable
* set: unordered, unique, mutable
* dict: unordered, unique key, mutable
* strings: ordered, immutable
* tuple: ordered, non-unique, immutable

### What is Understore _ 
https://hackernoon.com/understanding-the-underscore-of-python-309d1a029edc


### In Python, what is the difference between a generator  expression and a list comprehension?
Generator evaluates a next on call, list evaluates and stores all results in one shot.

For example,
Example of list comprehension: [x*2 for x in range(10) if x%2]
Example of generator expression: (x*2 for x in range(10) if x%2)

Notes: In Python 3.7, range is implemented as lazy generator, so no more xrange

### Return a list with unique element
```
# order is not important
def solution(L):
    return list(set(L))
L=[1,2,2,3,3,4]
print(solution(L))
```
```
# order is important
def solution(L):
    newset=set()
    l=[]
    print(newset)
    for i in L:
        if i not in newset:
            l.append(i)
            newset.add(i)
    return l

l=[2,2,1,3,3,4,5,6,7,7]
print(solution(l))
```
