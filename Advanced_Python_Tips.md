# Python copy object (shadow copy vs deep copy):
https://realpython.com/copying-python-objects/

* Making a shallow copy of an object won’t clone child objects. Therefore, the copy is not fully independent of the original.
* A deep copy of an object will recursively clone child objects. The clone is fully independent of the original, but creating a deep copy is slower.
* You can copy arbitrary objects (including custom classes) with the copy module.
