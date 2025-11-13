# swift-study

## Variables
- two variables "let" and "var"
- "let" is a constant value - cannot reassigned or change the value (data types/structure)
    - Exception however, if the value assigned to the ``let`` variable initially is a class, then internal value can be changed. e.g.; class
- "var" can be reassigned to new value


### Immutabilities on ``array`` or ``collection`` in swift
- declaring an array with keyword ``var`` will allow reassignment and modification of the contents of array
- declaring an array with keyword ``let`` will **NOT** allow for reassignment or modification of array
    - Modifcation may be allowed to ``let`` if the array value was initialized as a ``Class Type``

example: 
``
someText
``
