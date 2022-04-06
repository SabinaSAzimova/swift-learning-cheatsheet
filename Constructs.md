<h1 align="center"> Constructs </h1>
<h3 align="center"> Structures </h3>

**1.Structure Creation**

Structures, or structs, are used to programmatically represent a real-life object in code. Structures are created with the struct keyword followed by its name and then body containing its properties and methods.
```swift
struct Building {
  var address: String
  var floors: Int
 
  init(address: String, floors: Int, color: String) {
    self.address = address
    self.floors = floors
  }
}
```
----------------------------------------------------------------
**2.Default Property Values**

A structure’s properties can have preassigned default values to avoid assigning values during initialization. Optionally, these property’s values can still be assigned a value during initialization.
```swift
struct Car {
  var numOfWheels = 4
  var topSpeed = 80
}
 
var reliantRobin = Car(numOfWheels: 3)
 
print(reliantRobin.numOfWheels) // Prints: 3
print(reliantRobin.topSpeed)    // Prints: 80
```
----------------------------------------------------------------
**3.Structure Instance Creation**

A new instance of a structure is created by using the name of the structure with parentheses () and any necessary arguments.
```swift
struct Person {
  var name: String
  var age: Int
 
  init(name: String, age: Int) {
    self.name = name
    self.age = age
  }
}
 
// Instance of Person:
var morty = Person(name: "Morty", age: 14)
```
----------------------------------------------------------------
**4.Checking Type**

The built-in function type(of:) accepts an argument and returns the type of the argument passed.
```swift
print(type(of: "abc")) // Prints: String
print(type(of: 123))   // Prints: 123
```
----------------------------------------------------------------
**5.init() Method**

Structures can have an init() method to initialize values to an instance’s properties. Unlike other methods, The init() method does not need the func keyword. In its body, the self keyword is used to reference the actual instance of the structure.
```swift
struct TV {
  var screenSize: Int
  var displayType: String
  
  init(screenSize: Int, displayType: String) {
    self.screenSize = screenSize
    self.displayType = displayType
  }
}
 
var newTV = TV(screenSize: 65, displayType: "LED")
```
----------------------------------------------------------------
**6.Structure Methods**

Methods are like functions that are specifically called on an instance. To call the method, an instance is appended with the method name using dot notation followed by parentheses that include any necessary arguments.
```swift
struct Dog {
  func bark() {
    print("Woof")
  }
}
 
let fido = Dog()
fido.bark() // Prints: Woof
```
----------------------------------------------------------------
**7.Mutating Methods**

Structure methods declared with the mutating keyword allow the method to affect an instance’s own properties.
```swift
struct Menu {
  var menuItems = ["Fries", "Burgers"]
 
  mutating func addToMenu(dish: String) {
    self.menuItems.append(dish)
  }
}
 
var dinerMenu = Menu()
 
dinerMenu.addToMenu(dish: "Toast")
print(dinerMenu.menuItems) 
// Prints: ["Fries", "Burgers", "Toast"]
```
----------------------------------------------------------------
<h3 align="center"> Classes </h3>

**8.Swift Class**

A class is used to programmatically represent a real-life object in code. Classes are defined by the keyword class followed by the class name and curly braces that store the class’s properties and methods.
```swift
// Using data types:
class Student {
  var name: String
  var year: Int
  var gpa: Double
  var honors: Bool
}
 
 
// Using default property values:
class Student {
  var name = ""
  var year = 0
  var gpa = 0.0
  var honors = false
}
```
----------------------------------------------------------------
**9.Instance of a Class**

Creating a new instance of a class is done by calling a defined class name with parentheses () and any necessary arguments.
```swift
class Person {
  var name = ""
  var age = 0
}
 
var sonny = Person()
 
// sonny is now an instance of Person
```
----------------------------------------------------------------
**10.Class Properties**

Class properties are accessed using dot syntax, i.e. .property.
```swift
var ferris = Student()
 
ferris.name = "Ferris Bueller"
ferris.year = 12
ferris.gpa = 3.81
ferris.honors = false
```
----------------------------------------------------------------
**11.init() Method**

Classes can be initialized with an init() method and corresponding initialized properties. In the init() method, the self keyword is used to reference the actual instance of the class assign property values.
```swift
class Fruit {
  var hasSeeds = true 
  var color: String
 
  init(color: String) {
    self.color = color
  }
}
 
let apple = Fruit(color: "red")
```
----------------------------------------------------------------
**12.Inheritance**

A class can inherit, or take on, another class’s properties and methods:
The new inheriting class is known as a subclass.
The class that the subclass inherits from is known as its superclass.
```swift
// Suppose we have a BankAccount class:
 
class BankAccount {
  var balance = 0.0
 
  func deposit(amount: Double) {
    balance += amount
  }
 
  func withdraw(amount: Double) {
    balance -= amount
  }
}
 
 
// And we want a new SavingsAccount class that inherits from BankAccount:
 
class SavingsAccount: BankAccount {
  var interest = 0.0
 
  func addInterest() {
    let interest = balance * 0.005
    self.deposit(amount: interest)
  }
}
 
// Here, the new SavingsAccount class (subclass) automatically gains all of the characteristics of BankAccount class (superclass). In addition, the SavingsAccount class defines a .interest property and a .addInterest() method.
```
----------------------------------------------------------------
**13.Overriding**

A subclass can provide its own custom implementation of a property or method that is inherited from a superclass. This is known as overriding.
```swift
// Suppose we have a BankAccount class:
 
class BankAccount {
  var balance = 0.0
 
  func deposit(amount: Double) {
    balance += amount
  }
 
  func withdraw(amount: Double) {
    balance -= amount
  }
}
 
 
// Suppose we want a new SavingsAccount class and we want to override the .withdraw() method from its superclass BankAccount:
 
class SavingsAccount: BankAccount {
  var interest = 0.0
  var numWithdraw = 0
 
  func addInterest() {
    let interest = balance * 0.01
    self.deposit(amount: interest)
  }
 
  override func withdraw(amount: Double) {
    balance -= amount
    numWithdraw += 1
  }
}
```
----------------------------------------------------------------
**14.Reference Types**

Classes are reference types, while structures are value types, classes are reference types.
Unlike value types, reference types are not copied when they are assigned to a variable or constant, or when they are passed to a function. Rather than a copy, a reference to the same existing instance is used.

----------------------------------------------------------------























