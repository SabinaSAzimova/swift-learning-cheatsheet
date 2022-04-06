<h1 align="center"> Control flow </h1>

**1.if Statement**

An if statement executes a code block when its condition evaluates to true. If the condition is false, the code block does not execute.

```swift
var halloween = true 
 
if halloween {
  print("Trick or treat!")
}
```
 Prints: Trick or treat! 

---------------------------------------------------------------- 
**2.else Statement**

An else statement is a partner to an if statement. When the condition for the if statement evaluates to false, the code within the body of the else will execute.
```swift
var turbulence = false 
 
if turbulence {
  print("Please stay seated.")
} else {
  print("You may freely move around.")
}
 ```
 Prints: You may freely move around.

----------------------------------------------------------------
**3.else if Statement**

An else if statement provides additional conditions to check for within a standard if/else statement. else if statements can be chained and exist only after an if statement and before an else.
```swift
var weather = "rainy" 
 
if weather == "sunny" {
  print("Grab some sunscreen")
} else if weather == "rainy" {
  print("Grab an umbrella")
} else if weather == "snowing" {
  print("Wear your snow boots")
} else {
  print("Invalid weather")
}
```
 
 Prints: Grab an umbrella

----------------------------------------------------------------

**4.switch Statement**

The switch statement is a type of conditional used to check the value of an expression against multiple cases. A case executes when it matches the value of the expression. When there are no matches between the case statements and the expression, the default statement executes.
```swift
var secondaryColor = "green"
 
switch secondaryColor {
  case "orange":
    print("Mix of red and yellow")
  case "green":
    print("Mix of blue and yellow")
  case "purple":
    print("Mix of red and blue") 
  default: 
    print("This might not be a secondary color.") 
}
 ```
 Prints: Mix of blue and yellow
 
 ----------------------------------------------------------------
**5.switch Statement: Interval Matching**

Intervals within a switch statement’s case provide a range of values that are checked against an expression.
```swift
let year = 1905
var artPeriod: String
 
switch year {
  case 1860...1885:
    artPeriod = "Impressionism"
  case 1886...1910:
    artPeriod = "Post Impressionism"
  case 1912...1935: 
    artPeriod = "Expressionism"
  default:  
    artPeriod = "Unknown"
}
 ```
 Prints: Post Impressionism
 
 ----------------------------------------------------------------
**6.switch Statement: Compound Cases**

A compound case within a switch statement is a single case that contains multiple values. These values are all checked against the switch statement’s expression and are separated by commas.
```swift
let service = "Seamless"
 
switch service {
  case "Uber", "Lyft":
    print("Travel")
  case "DoorDash", "Seamless", "GrubHub":
    print("Restaurant delivery")
  case "Instacart", "FreshDirect":
    print("Grocery delivery")
  default: 
    print("Unknown service")
}
```
 Prints: Restaurant delivery
 
 ----------------------------------------------------------------
**7.switch Statement: where Clause**

Within a switch statement, a where clause is used to test additional conditions against an expression.
```swift
let num = 7
 
switch num {
  case let x where x % 2 == 0:
    print("\(num) is even")
  case let x where x % 2 == 1:
    print("\(num) is odd")
  default:
    print("\(num) is invalid")
}
```
 Prints: 7 is odd
 
----------------------------------------------------------------
**8.Ternary Conditional Operator**

The ternary conditional operator, denoted by a ?, creates a shorter alternative to a standard if/else statement. It evaluates a single condition and if true, executes the code before the :. If the condition is false, the code following the : is executed.
```swift
var driverLicense = true
 
driverLicense ? print("Driver's Seat") : print("Passenger's Seat") 
```
Prints: Driver's Seat

----------------------------------------------------------------
**9.Ranges**

Ranges created by the ... operator will include the numbers from the lower bound to (and includes) the upper bound.
```swift
let zeroToThree = 0...3
 ```
zeroToThree: 0, 1, 2, 3

----------------------------------------------------------------
**10.stride() Function**

Calling stride() with the 3 necessary arguments creates a collection of numbers; the arguments decide the starting number to, the (excluded) ending number, and how to increment/decrement from the start to the end.
```swift
for oddNum in stride(from: 1, to: 5, by: 2) {
  print(oddNum)
}
 ```
Prints: 1

Prints: 3

 ----------------------------------------------------------------
**11.for-in Loop**

The for-in loop is used to iterate over collections, including strings and ranges.
```swift
for char in "hehe" {
  print(char)
}
 ```
Prints: h

Prints: e

Prints: h

Prints: e

----------------------------------------------------------------
**12.continue Keyword**

The continue keyword will force the loop to move on to the next iteration.
```swift
for num in 0...5 {
  if num % 2 == 0 {
    continue
  }
  print(num)
}
 ```
Prints: 1

Prints: 3

Prints: 5

----------------------------------------------------------------
**13.break Keyword**

To terminate a loop before its completion, use the break keyword.
```swift
for char in "supercalifragilisticexpialidocious" {
  if char == "c" {
    break
  }
  print(char)
}
 ``````
Prints: s

Prints: u

Prints: p

Prints: e

Prints: r

 ----------------------------------------------------------------
**14.Using Underscore**

Use _ instead of a placeholder variable if the variable is not referenced in the for-in loop body.
```swift
for _ in 1...3 {
  print("Olé")
}
 ```
Prints: Olé

Prints: Olé

Prints: Olé

----------------------------------------------------------------
**15.while Loop**

A while loop accepts a condition and continually executes its body’s code for as long as the provided condition is true.

If the condition is never false then the loop continues to run and the program is stuck in an infinite loop.
```swift
var counter = 1
var stopNum = Int.random(in: 1...10)
 
while counter < stopNum {
  print(counter)
  counter += 1
}
 ```
The loop prints until the stop condition is met

----------------------------------------------------------------
