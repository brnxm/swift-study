# swift-study

## Variables
- Two keywords for defining a variable, ``var`` and ``let``
- ``let`` is a constant value - cannot reassigned or change the value (data types/structure)
    - Exception however, if the value assigned to the ``let`` variable initially is a class, then internal value can be changed. e.g.; class
- ``var`` can be reassigned to new value with the same Type as previously defined

## Types
### Int
- 62-bit on modern devices
- signed by default
- uses Int64 by default
Best practice: Use ``Int`` unless you need a specific size or unsigned
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
let unicode = "café ☕️ cost $5"
```

Useful properties/methods:
```swift
name.count
name.isEmpty
name.uppercased()     // mutates the name variable
name.contains("Swift")     // Checks a substring of "Swift"
name.hasPrefix("Tay")
```
String interpolation:
- Process of embedding expressions or variables directly in string literals using the ``\( )`` syntax.
```swift
let score = 95
let message = "Your score is \(score * 2) points!"
```
### Character
A single grapheme cluster:
```swift
let letter: Character = "A"     // a single character literal is String
let flag = "🇺🇸"    // one Character (flag is a single grapheme cluster)
```
Must explicitly specify ``Character`` type to a variable, a single character literal will inferred as ``String``

### Type inference
Swift infers types when possible
```swift
let x = 42     // Int
let y = 3.14    // Double
let z = "Hello"    // String
let flag = true    // Bool
```

### Type Aliases
typealias AudioSample = UInt16
typealias UserID = String
var sample: AudioSample = 2048

### Tuples
lightweight grouping of values (unnamed struct-like):
```swift
let http404 = (404, "Not found")    // (Int, String)
let coordinates = (x: 10.5, y: 20.3)    // labeled
let (statusCode, message) = http404    // decomposition

print(coordinates.x)     // 10.5
print(http404.0)    // 404 (by position)
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

## Code reading comprehension
### Calling closures
#### Calling in the arguments 
```swift
myFunc(closure: { $0 + $1 } )
```
#### Trailing closure
```swift
myFunc() { $0 + $1 }

// if function only contains the closure, can omit the argument parenthesis
myFunc { $0 + $1 }
```

### ``rethrows`` keyword
- ``rethrows`` keyword can be seen only in function/method declaration
- it indicates that there is a closure in the parameters that **may or may not** throw
```swift
// declaration with rethrows
func performMath(closure: (Int, Int) throws -> Int ) rethrows -> Int { ... }
```

## SwiftUI framework
- // Recursive type constraints
- // leaf node - terminating recursion by using Never?

# Notes/Good to know
## Differences between attribute and macros
### Attributes
- Provide metadata about declarations (classes, structs, enums, properties, functions, etc)
- Influences the compiler how the system treats the declaration
### Macros
- Compile-time code generation mechanism.
- Code generation - actively generate new declarations, add protocol conformances, introduce members or modify properties
