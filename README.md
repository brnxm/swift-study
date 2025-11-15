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
 
## Operators
### unary prefix operator
### unary post fix operator
### binary infix operator
### ternary operator
### operands/expressions/operators
| Expression | Operator | Operands |
|---|---|---|
|5 + 3 | + | 5, 3|
|-x| - | x|
|a && b| && | a,b|
|c ? x : y| ?: |c,y,x|
- ``Operands``- the value being operated
- ``Operator``- the operation (action)
- ``Expression`` - single group or instance of operand/s and an operator


## Control Flow
- Operators in ``if-else`` statement
- ``&&``- logical **AND** operator
- ``||``- logical **OR** operator
- operator ``&&`` takes precedence over ``||`` operator, ``&&`` operator binds two boolean expression to form a single logical group (expression). For example;
```
a > b && c < d
```
- there is two statement, ``a > b`` and ``c < d``, binded by ``&&`` in the middle, making the two expressions as a single logical expression
