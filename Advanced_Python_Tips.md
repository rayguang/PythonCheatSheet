### Python copy object (shadow copy vs deep copy):
https://realpython.com/copying-python-objects/

* Making a shallow copy of an object won’t clone child objects. Therefore, the copy is not fully independent of the original.
* A deep copy of an object will recursively clone child objects. The clone is fully independent of the original, but creating a deep copy is slower.
* You can copy arbitrary objects (including custom classes) with the copy module.

* Shadow Copy
```
import copy
xs = [1,2,3]
ys = copy.copy(xs)
```
OR
```
ys = list(xs)
```

* Deep Copy
```
import copy
ys = copy.deepcopy(xs)
```

### Why tuple is faster than list
* tuple is immutable, therefore stores in a fixed size of block of memory and does not require any more space to store additional data. List is mutable and consists of two blocks: one block stores all object information and the other VARIABLE sized block stores all the data. Therefore,
** Indexing of tuple is faster than list (slightly faster).  
** Creating the tuple object is faster than list. 

* tuple is immutable, but its member might be still mutable, see example below:
```
a=[1,2,4]
b=['a','b']
tupled_list=(a,b)
a.append(5)
b.append('c')
```

Output is:
```
([1, 2, 4, 5], ['a', 'b', 'c'])
```

### Closure Pattern
* What: A nested function reference a value in its enclosing scope. The value in the enclosing scope is remembered even if the variable goes out of the scope or the function itself is removed from the current namespace.
** We must have a nested function (function within function)
** The nested function must reference a value in ints enclosing scope
** The enclosing function must return the nested function.

For example, 
```
def print_msg(msg):
# Outer enclosing scope

    def printer():
    # Nested function
        print(msg)

    return printer


another = print_msg('hello')
another()
```
