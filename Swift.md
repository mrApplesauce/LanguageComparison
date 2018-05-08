# Swift

## Language Purpose/Genesis
#### Why was the language created?
Swift was created as a programming language to be used by developers on any of Apple's platforms including iOS, macOS, and many others.
#### What problems was the language trying to address?
Swift was made to address many of the common issues faced in programming. One of these issues was null pointers and crashes as a result of dereferencing them. Additionally, the language tries to simplify syntax by making it more intuitive and easy to read.
#### Is the language a reaction to a previous language or a replacement for another language?
Swift was a replacement for Objective-C which had been previously used by developers on Apple platforms.

## Unique Features of the Language

## Name Spaces
#### How are nemespaces implemented?
Swift does not currently support namespace types within modules.
#### How are namespaces used?
Swift does not currently support namespace types within modules.

## Types
#### What types does the language support?
The data types supported by Swift are Int, Double, Float, Bool, String, Character, Optional, Array, Dictionary, Structure, and Class.
#### Are both reference and value types supported?
Swift supports both reference and value types.
#### Can new value types be created?
New classes are reference variables so no new value types can be created in Swift.


## Classes
#### Defining
```
class Animal() {
    var name = "Giraffe"
    func description() -> {
        return "this animal is a \(name)."
    }
}
```
#### Creating new instances
```
var animal = Animal()
```
#### Constructing/initializing
The initializer is defined with the init function within the class.
```
class Animal() {
    let name: String
    
    init (name: String) {
        self.name = name
    }
    
    func description() -> {
        return "this animal is a \(name)."
    }
}
```
#### Destructing/de-initializing
A deinitializer is called immediately before a class instance is deallocated.

## Instance reference name in data type
To reference the instance within the class, use the instance reference name 'self'.

## Properties
#### Getters and setters... write your own or built in?
Getters and Setters are defined on primitive data types by default as:
```
var getAge = Student.age  //example of getting a class property
Student.age = getAge  //example of setting a class property
```
Getters and setters can be set on a variable as follows:
```
var age: Int {
    get {
        //defines the return value for age
    }
    set (newValue) {
        //defines the functionality for setting age
    }
}
```
#### Backing variables?
An instance variable can be used to back the value stored in a class property.
#### Computed properties?
Computed properties give developers getters and setters that can be used to indirectly retrieve and set variable values.

## Interfaces/ Protocols
#### What does the languge support?
Protocols in Swift allow for the blueprinting of methods, properties, and other requirements that a class or struct should implement.
#### What abilities does it have?
Protocols can be used to define what methods (including their signature), properties, and various other requirements must be implemented within a certain class or struct.
#### How is it used?
An example of a class using a protocol follows:
```
protocol ProtocolName() {
    func someFunction() -> Int
}

class ClassName(): ProtocolName {
    func someFunction() -> Int {
        var num: Int = 0
        return num
    }
}
```

## Inheritance/ Extension
Extension is used in Swift. An example of an extension to the Double class follows:
```
extension Double {
   var doubled: Double {return self * 2}
}
let doubleNum: Double = 12.1.doubled
```

## Reflection
#### What reflection abilities are supported?
Reflection in Swift is based around a struct called Mirror. Instantiating a mirror on a subject allows you to then use that mirror to query your subject.
#### How is reflection used?
```
let mirror = Mirror(reflecting: subject)
print(mirror)
```

## Memory Management
#### How is it handled?
Automatic reference counting is used in Swift meaning that for the majority of cases, memory management will work without any instruction from the developer.
#### How does it work?
As previously mentioned, the automatic reference counting keeps track of the current references kept by the program and automatically allocates and deallocates memory as needed.
#### Garbage collection?
When there are no longer any references to an instance, that instance is then automatically deallocated to free up space in memory.
#### Automatic reference counting?
Automatic reference counting is the mechanism at the center of Swift's memory management.

## Comparisons of References and Values
#### How are values compared?

## Null/Nil References
#### Which does the language use?
#### Does the language have features for handling null/nil references?

## Errors and Exception Handling

## Lambda Expressions, Closures, or Functions as Types

### Implementation of Listeners and Event Handlers

## Singleton
#### How is a singleton implemented?
#### Can it be made thread-safe?
#### Can the singleton instance be lazily instantiated?

## Procedural Programming

## Functional Programming

## Multithreading
#### Threads or thread-like abilities
#### How is multitasking accomplished?
