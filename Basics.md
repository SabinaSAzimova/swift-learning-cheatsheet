<h1 align="center"> THE BASICS</h1>

1.print()

The print() function outputs one or more values to the terminal.

```swift
print("Hello World")
```

----------------------------------------------------------------
2.Single-line comment 

Single-line comments are created using two consecutive forward slashes. The compiler ignores any text after // on the same line.
```swift
// This is a single line comment.
```
----------------------------------------------------------------
3.Multiline Comments

Multiline comments are created using /* to begin the comment, and */  to end the comment. The compiler ignores any text in between.
```swift
/*
This is a 
multiline comment
*/
```
----------------------------------------------------------------
4.Program structure

The program runs line by line, from top to bottom:
```swift
print("Hola")
print("Buenos días")
```
Line 1 prints Hola

Line 2 prints Buenos días

----------------------------------------------------------------
5.Variables 

A variable refers to a storage location in the computer’s memory that one can set aside to save, retrieve, and manipulate data.
```swift
var score = 0
```
----------------------------------------------------------------
6.Constants

Constants refer to fixed values that a program may not alter during its execution. One can be declared by using the let keyword.
```swift
let pi = 3.14
```
----------------------------------------------------------------
7.Arithmetic operators

Swift supports arithmetic operators for:

* addition +
* subtraction -
* multiplication *
* division /
* remainder %
```swift
var x = 0
x = 4 + 2  // x is now 6
x = 4 - 2  // x is now 2
x = 4 * 2  // x is now 8
x = 4 / 2  // x is now 2
x = 4 % 2  // x is now 0
```
----------------------------------------------------------------
8.Types

Type annotation can be used during declaration.

The basic data types are:

* Int: integer numbers
* Double: floating-point numbers
* String: a sequence of characters
* Bool: truth values
```swift
var age: Int = 28
var price: Double = 8.99
var message: String = "good night"
var lateToWork: Bool = true
```
----------------------------------------------------------------
9.String Interpolation

String interpolation can be used to construct a String from a mix of variables, constants, and others by including their values inside a string literal.
```swift
var apples = 6
print("I have \(apples) apples!")
 ```
Prints: I have 6 apples!

----------------------------------------------------------------
10.Compound Assignment Operators

Compound assignment operators provide a shorthand method for updating the value of a variable:

* += add and assign the sum

* -= subtract and assign the difference

* *= multiply and assign the product

* /= divide and assign the quotient

* %= divide and assign the remainder
 ```swift
var numberOfDogs = 100
numberOfDogs += 1
print("There are \(numberOfDogs) dalmations!")
 ```

Prints: There are 101 dalmations!

----------------------------------------------------------------




























