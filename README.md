# swift-study

## Variables
- two variables "let" and "var"
- "let" is a constant value - cannot reassigned or change the value (data types/structure)
    - Exception however, if the value assigned to the ``let`` variable initially is a class, then internal value can be changed. e.g.; class
- "var" can be reassigned to new value

## Types
### Int
- 65-bit on modern devices
- signed by default
```swift
Int // using by default is Int64 on modern devices
Int8 // -128 to 127
Int16
Int32
Int64
UInt8 // 0 to 255
UInt64 // 18 sextillion (max possible integer)

let age: Int = 30
let maxValue: UInt32 = 4_294_967_295
```

### Floating-point numbers
- ``Float`` -> 32-bit precision (~6 decimal digits)
- ``Double`` -> 64-bit precision (~15 decimal digits) <- default for floating-point literals
```swift
let pi = 3.14159    // Double (inferred)
let e: Float = 2.71828     // explicitly float
let precise = 3.141592653589793    // still Double
```

### Boolean
- Only one type
- No truthy/falsy values like 0, "hello", etc. are not Bool
```swift
let isEnabled: Bool = true
let hasError = false    // inferred Bool
```

### String
- ``String`` is a ``value type`` and a collection of ``Character``
```swift
let name = "Taylor Swift"     // String literal
var mutable: String = " Hello"
mutable += " World"

let multiline = """
This is a
multiline string
"""
let unicode = "afé ☕️ cost
```

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
