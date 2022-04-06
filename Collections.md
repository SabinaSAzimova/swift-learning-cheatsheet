<h1 align="center"> Collections </h1>

<h3 align="center">Array</h3>

**1.Creating an Array**

An array stores an ordered collection of values of the same data type. Use the initializer syntax, [Type](), to create an empty array of a certain type.
```swift
var scores = [Int]()
 
// The array is empty: []
```

----------------------------------------------------------------
**2.Initialize with Array Literal**

An array can be initialized with an array literal, which is a short-hand method of writing one or more values as an array collection.

An array literal is written as a list of values, separated by commas, and surrounded by a pair of square brackets.
```swift
// Using type inference:
var snowfall = [2.4, 3.6, 3.4, 1.8, 0.0]
 
// Being explicit with the type:
var temp: [Int] = [33, 31, 30, 38, 44]
```

----------------------------------------------------------------
**3.Index**

An index refers to an item’s position within an ordered list. Use the subscript syntax, array[index], to retrieve an individual element from an array.

Note: Swift arrays are zero-indexed, meaning the first element has index 0.
```swift
var vowels = ["a", "e", "i", "o", "u"]
 
print(vowels[0])  // Prints: a
print(vowels[1])  // Prints: e
print(vowels[2])  // Prints: i
print(vowels[3])  // Prints: o
print(vowels[4])  // Prints: u
```

----------------------------------------------------------------
**4..count Property**

The .count property returns the number of elements in an array.
```swift
var grocery = ["🥓", "🥞", "🍪", "🥛", "🍊"]
 
print(grocery.count)
 
// Prints: 5
```

----------------------------------------------------------------
**5..append() Method and += Operator**

The .append() method can be called on an array to add an item to the end of the array.

The += addition assignment operator can be used to add the elements of another array to the existing array.
```swift
var gymBadges = ["Boulder", "Cascade"]
 
gymBadges.append("Thunder")
gymBadges += ["Rainbow", "Soul"]
 
// ["Boulder", "Cascade", "Thunder", "Rainbow", "Soul"]
```

----------------------------------------------------------------
**6..insert() and .remove() Methods**

The .insert() method can be called on an array to add an element at a specified index. It takes two arguments: value and at: index.

The .remove() method can be called on an array to remove an element at a specified index. It takes one argument: at: index.
```swift
var moon = ["🌖", "🌗", "🌘", "🌑"]
 
moon.insert("🌕", at: 0)
 
// ["🌕", "🌖", "🌗", "🌘", "🌑"]
 
moon.remove(at: 4)
 
// ["🌕", "🌖", "🌗", "🌘"]
```

----------------------------------------------------------------
**7.Iterating Over an Array**

In Swift, a for-in loop can be used to iterate through the items of an array.
This is a powerful tool for working with and manipulating a large amount of data.
```swift
var employees = ["Michael", "Dwight", "Jim", "Pam", "Andy"]
 
for person in employees {
  print(person)
}
 
// Prints: Michael
// Prints: Dwight
// Prints: Jim
// Prints: Pam
// Prints: Andy
```

----------------------------------------------------------------
<h3 align="center">Sets</h3>

**8.Swift Sets**

We can use a set to store unique elements of the same data type.
```swift
var paintingsInMOMA: Set = ["The Dream", "The Starry Night", "The False Mirror"]
```

----------------------------------------------------------------
**9.Empty Sets**

An empty set is a set that contains no values inside of it.
```swift
var team = Set<String>()
 
print(team)
// Prints: [] 
  ```
----------------------------------------------------------------
**10.Populated Sets**

To create a set populated with values, use the Set keyword before the assignment operator.

The values of the set must be contained within brackets [] and separated with commas ,.
```swift
var vowels: Set = ["a", "e", "i", "o", "u"]
  ```
  
----------------------------------------------------------------
**11..insert()**

To insert a single value into a set, append .insert() to a set and place the new value inside the parentheses ().
```swift
var cookieJar: Set = ["Chocolate Chip", "Oatmeal Raisin"]
 
// Add a new element
cookieJar.insert("Peanut Butter Chip")
 ```
----------------------------------------------------------------
**12..remove() and .removeAll() Methods**

To remove a single value from a set, append .remove() to a set with the value to be removed placed inside the parentheses ().

To remove every single value from a set at once, append .removeAll() to a set.
```swift
var oddNumbers: Set = [1, 2, 3, 5]
 
// Remove an existing element
oddNumbers.remove(2)
 
// Remove all elements
oddNumbers.removeAll()
  ```
----------------------------------------------------------------
**13..contains()**

Appending .contains() to an existing set with an item in the parentheses () will return a true or false value that states whether the item exists within the set.
```swift
var names: Set = ["Rosa", "Doug", "Waldo"]
 
print(names.contains("Lola")) // Prints: false
 
if names.contains("Waldo"){
  print("There's Waldo!")
} else {
  print("Where's Waldo?")
}
// Prints: There's Waldo!
  ```
----------------------------------------------------------------
**14.Iterating Over a Set**

A for-in loop can be used to iterate over each item in a set.
```swift
var recipe: Set = ["Chocolate chips", "Eggs", "Flour", "Sugar"]
 
for ingredient in recipe {
  print ("Include \(ingredient) in the recipe.")
}
  ```
----------------------------------------------------------------
**15..isEmpty Property**

Use the built-in property .isEmpty to check if a set has no values contained in it.
```swift
var emptySet = Set<String>()
 
print(emptySet.isEmpty)  // Prints: true
 
var populatedSet: Set = [1, 2, 3]
 
print(populatedSet.isEmpty) // Prints: false
 ``` 
----------------------------------------------------------------
**16..count Property**

The property .count returns the number of elements contained within a set.
```swift
var band: Set = ["Guitar", "Bass", "Drums", "Vocals"]
 
print("There are \(band.count) players in the band.")
// Prints: There are 4 players in the band.
  ```
----------------------------------------------------------------
**17..intersection() Operation**

The .intersection() operation populates a new set of elements with the overlapping elements of two sets.
```swift
var setA: Set = ["A", "B", "C", "D"]
var setB: Set = ["C", "D", "E", "F"]
 
var setC = setA.intersection(setB)
print(setC)  // Prints: ["D", "C"]
  ```
----------------------------------------------------------------
**18..union() Operation**

The .union() operation populates a new set by taking all the values from two sets and combining them.
```swift
var setA: Set = ["A", "B", "C", "D"]
var setB: Set = ["C", "D", "E", "F"]
 
var setC = setA.union(setB)
print(setC) 
// Prints: ["B", "A", "D", "F", "C", "E"]
```
  
----------------------------------------------------------------
**19..symmetricDifference() Operation**

The .symmetricDifference() operation creates a new set with all the non-overlapping values between two sets.
```swift
var setA: Set = ["A", "B", "C", "D"]
var setB: Set = ["C", "D", "E", "F"]
 
var setC = setA.symmetricDifference(setB)
print(setC) 
// Prints: ["B", "E", "F", "A"]
  ```
----------------------------------------------------------------
**20..subtracting() Operation**

The .subtracting() operation removes the values of one second set from another set and stores the remaining values in a new set.
```swift
var setA: Set = ["A", "B", "C", "D"]
var setB: Set = ["C", "D"]
 
var setC = setA.subtracting(setB)
print(setC) 
// Prints: ["B", "A"]
  ```
----------------------------------------------------------------
<h3 align="center">Dictionary</h3>

**21.Dictionary type**

A dictionary is an unordered collection of paired data, or key-value pairs.
```swift
var dictionaryName = [
  "Key1": "Value1",
  "Key2": "Value2",
  "Key3": "Value3"
]
```
----------------------------------------------------------------
**22.Keys**

Every key in a dictionary is unique.
Keys can be be used to access, remove, add, or modify its associated value.
```swift
// Each key is unique even if they all contain the same value
 
var fruitStand = [
  "Coconuts": 12,
  "Pineapples": 12,
  "Papaya": 12
]
```
 ----------------------------------------------------------------
 
**23.Type Consistency**

In a dictionary, the data type of the keys and the values must remain consistent.
```swift
// Contains only String keys and Int values
 
var numberOfSides = [
  "triangle": 3,
  "square": 4,
  "rectangle": 4
]
```
----------------------------------------------------------------
**24.Initialize a Populated Dictionary**

Dictionary literals contain lists of key-value pairs that are separated by commas; this syntax can be used to create dictionaries that are populated with values.
```swift
var employeeID = [
  "Hamlet": 1367,
  "Horatio": 8261,
  "Ophelia": 9318
]
```
----------------------------------------------------------------
**25.Initialize an Empty Dictionary**

An empty dictionary is a dictionary that contains no key-value pairs.
There is more than one way to initialize an empty dictionary; the method chosen is purely up to preference and makes no impact on the dictionary.
```swift
// Initializer syntax:
var yearlyFishPopulation = [Int: Int]()
 
// Empty dictionary literal syntax:
var yearlyBirdPopulation: [Int: Int] = [:]
 ```
 ----------------------------------------------------------------
**26.Adding to a Dictionary**

To add a new key-value to a dictionary, use subscript syntax by adding a new key contained within brackets [ ] after the name of a dictionary and a new value after the assignment operator (=).
```swift
var pronunciation = [
  "library": "lai·breh·ree",
  "apple": "a·pl"
]
 
// New key: "programming", New value: "prow·gra·muhng"
pronunciation["programming"] = "prow·gra·muhng"
```
----------------------------------------------------------------
**27.Removing Key-Value Pairs**

To remove a key-value pair from a dictionary, set the value of a key to nil with subscript syntax or use the.removeValue() method.
To remove all the values in a dictionary, append .removeAll() to a dictionary.
```swift
var bookShelf = [
  "Goodnight Moon": "Margaret Wise Brown",
  "The BFG": "Roald Dahl",
  "Falling Up": "Shel Silverstein",
  "No, David!": "David Shannon"
]
 
// Remove value by setting key to nil
bookShelf["The BFG"] = nil
 
// Remove value using .removeValue()
bookShelf.removeValue(forKey: "Goodnight Moon")
 
// Remove all values
bookShelf.removeAll()
```
----------------------------------------------------------------
**28.Modifying Key-Value Pairs**

To change the value of a key-value pair, use the .updateValue() method or subscript syntax by appending brackets [ ] with an existing key inside them to a dictionary’s name and then adding an assignment operator (=) followed by the modified value.
```swift
var change = [
  "Quarter": 0.29,
  "Dime": 0.15,
  "Nickel": 0.05,
  "Penny": 0.01
]
 
// Change value using subscript syntax
change["Quarter"] = .25
 
// Change value using .updateValue()
change.updateValue(.10, forKey: "Dime")
```
----------------------------------------------------------------
**29..isEmpty Property**

The .isEmpty property will return a true value if there are no key-value pairs in a dictionary and false if the dictionary does contain key-value pairs.
```swift
var bakery = [String:Int]() 
 
// Check if dictionary is empty
print(bakery.isEmpty)  // Prints true
 
bakery["Cupcakes"] = 12  
 
// Check if dictionary is empty
print(bakery.isEmpty)  // Prints false
```
----------------------------------------------------------------
**30..count Property**

The .count property returns an integer that represents how many key-value pairs are in a dictionary.
```swift
var fruitStand = [
  "Apples": 12,
  "Bananas": 20,
  "Oranges", 17
]
 
print(fruitStand.count)  // Prints: 3
```
----------------------------------------------------------------
**31.Assigning a Value to a Variable**

To assign the value of a key-value pair to a variable, set the value of a variable to dictionaryName[keyValue].

Note: Assigning the value of a key-value pair to a variable will return an optional value. To extract the value, use optional unwrapping.
```swift
var primaryHex = [
  "red": "#ff0000",
  "yellow": "#ffff00",
  "blue": "#0000ff",
]
 
print("The hex code for blue is \(primaryHex["blue"])")
// Prints: The hex code for blue is Optional("#0000ff")
 
if let redHex = primaryHex["red"] {
  print("The hex code for red is \(redHex)")
}
// Prints: The hex code for red is #ff0000
```
----------------------------------------------------------------
**32.Iterating Over a Dictionary**

A for-in loop can be used to iterate through the keys and values of a dictionary.
```swift
var emojiMeaning = [
  "🤔": "Thinking Face",
  "😪": "Sleepy Face",
  "😵": "Dizzy Face"
]
 
// Iterate through both keys and values
for (emoji, meaning) in emojiMeaning {
  print("\(emoji) is known as the '\(meaning) Emoji'")
}
 
// Iterate only through keys
for emoji in emojiMeaning.keys {
  print(emoji)
}
 
// Iterate only through values
for meaning in emojiMeaning.values {
  print(meaning)
}
```
----------------------------------------------------------------
