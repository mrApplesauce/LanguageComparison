# Java

## Language Purpose/Genesis
#### Why was the language created?
Java was created by James Gosling who needed to create a programming language that could run on multiple appliances with as little overhead as possible and what he ended up creating was Java.
#### What problems was the language trying to address?
Java was made to be a code that could easily be run on any platform with support of Java without any recompiling. This means that implementation was easier than that of previous codes. Additionally, with object oriented programming in mind, Java was built entirely around this framework making development of object oriented programs much easier than it had been in the past.
#### Is the language a reaction to a previous language or a replacement for another language?
Java was not a direct replacement for any language but it took many of its features from C and C++.

## Unique Features of the Language
Java is entirely focused on being an object oriented language. Everything in Java must be embedded within a class, which is not something you see in a lot of more modern, multi-paradigm languages.

## Name Spaces
#### How are nemespaces implemented?
Files in Java are organized with classes at the lowest level. These classes are then organized into packages which contain related classes.
#### How are namespaces used?
Namespaces work to limit the scope of programs and the level of access a given class can have. Classes within a package can utilize code from one another while classes from different packages cannot.

## Types
#### What types does the language support?
The primitive data types in Java are boolean, byte, char, short, int, long, float, and double. Java also supports packages, classes, interfaces, as well as other reference types.
#### Are both reference and value types supported?
Java supports both reference and value types.
#### Can new value types be created?
In Java, you can make a new class object; however, in doing so, you are creating a reference type and not a value type. Creating a new value type in Java is not possible.

## Classes
#### Defining
A new class is defined by creating a new file of type class. A class looks like the following:
```
public class MyClass {
    //this is the class block
}
```
#### Creating new instances
Instantiating new instances is done using the 'new' keyword and looks like the following:
```
MyClass myClass = new MyClass();
```
#### Constructing/initializing
The constructor is defined within the class. There can be multiple different constructors with different signatures. Examples of constructors follow:
```
public class MyClass {
    private int num;
    public MyClass(newNum) {
        num = newNum;
    }
}
```
#### Destructing/de-initializing
The garbage collector in Java automatically takes care of any object without a reference. When there are no references to an object left, that object's space in memory is deallocated and made available for future use.

## Instance reference name in data type
Java uses the keyword 'this' when referencing an instance from wihtin the class.

## Properties
#### Getters and setters... write your own or built in?
Java provides no default getters or setters. Developers are responsible for writing getters and setters for any of the attributes of a class.
#### Backing variables?
A private variable can be used to store the value stored in a publicly available field. This way the private variable works as a backing variable.
#### Computed properties?
Methods defined within a class can be used to return computed properties based on the fields of the class.

## Interfaces/ Protocols
#### What does the languge support?
Java supports interfaces.
#### What abilities does it have?
Interfaces in Java have the ability to define the signatures of methods that must be implemented in a class as well as any variables that need to be defined within the class.
#### How is it used?
Here is an example of an interface being defined:
```
public interface MyInterface {
    void doSomething();
}
```
Implementing that interface would then look like the following:
```
public class MyClass implements MyInterface {
    void doSomething() {
        //code to do something
    }
}
```

## Inheritance/ Extension
Java uses inheritance to extend the functionality of a class. A subclass can inherit variables, constructors, and methods from a superclass. From there, methods can be overwritten or overloaded to provide still further adaptability. Using inheritance can look like the following:
```
public class SuperClass {
    private String str;
    public SuperClass() {
        this.str = "Hello";
    }
}

public class SubClass {
    public SubClass() {
        this.str = "Goodbye";
    }
}
```

## Reflection
#### What reflection abilities are supported?
Java has reflection built in to access information on classes, methods, and fields during runtime of a program.
#### How is reflection used?
To get information for reflection at run time, the Class, Method, and Field types must be utilized like they are in the example below:
```
Class myClass = anObject.class;
Method[] methods = myClass.getMethods();
Field[] fields = myClass.getFields();
```
Information about each of these can then be found within attributes within these classes.

## Memory Management
#### How is it handled?
Java's memory management is automatically taken care of by a garbage collector.
#### How does it work?
The garbage collector checks for objects that are no longer being referenced, and when it finds such an object it automatically deallocates the memory being used by that object and makes it available reuse.
#### Garbage collection?
As mentioned previously, Java uses a garbage collector to manage its memory usage.
#### Automatic reference counting?
Unlike Swift, Java does not utilize automatic reference counting in its management of memory.

## Comparisons of References and Values
#### How are values compared?
In Java, == compares the objects referenced by the two variables being compared. On the other hand, the .equals() method compares the values stored in the objects referenced by variables so it works for strings as well as primitive data types.

## Null/Nil References
#### Which does the language use?
Java uses the keyword 'null'.
#### Does the language have features for handling null/nil references?
Java does not have any built in way to references to null values. The only way to check if a value is null is to check with == NULL. The ability to easily dereference null values causes crashes and is a reason for the development of programming tools like optionals.

## Errors and Exception Handling
Try catch statements are used for catching exceptions. Within the try clause, statements are written that may throw exceptions. After the try statement, catch clauses are used to handle any exceptions thrown by the try clause. The catch statements have to be in order from most specific to more general exceptions otherwise the more general exceptions will always be triggered before the more specific ones. Additionally the 'throws' keyword can be used to signify that a class or method can disregard a certain type of exception.

## Lambda Expressions, Closures, or Functions as Types
Lambda expressions can be expressed as functional interfaces in Java. An example of creating a lambda from a functional interface is included below:
```
public interface MyFunction {
    public boolean compare (int num1, int num2);
}

MyFunction myFunction = (num1, num2) -> return num1 > num2;
```

### Implementation of Listeners and Event Handlers
There are multiple ways to implement event handlers in Java. Two of those ways include using lambda expressions and anonymous inner classes. Below is an example of setting up an event handler using a lambda expression where subject is the value to attach a listener to:
```
subject.addListener(ObservableValue<? extends Number> observable, Number oldValue, final Number newValue) -> {
    //code to be exectured when a change occurs in the value of subject
});
```

## Singleton
#### How is a singleton implemented?
A singleton can be implemented like the following:
```
class Singleton {
    private static Singleton instance;
    private Singleton () {
        //private constructor
    }
    public static synchronized Singleton getInstance() {
        if (instance == null)
            instance = new Singleton();
            
        return instance;
    }
}
```
#### Can it be made thread-safe?
The 'synchronized' keyword on the getInstance() method means that this Singleton would work in a threaded environment.
#### Can the singleton instance be lazily instantiated?
By using a double locking mechanism where the synchronized keyword is only used in the case of a null instance, lazy instantiation can be implemented and will increase performance of the singleton.

## Procedural Programming
Procedural programming simply means that the code is executed on command after another. Although Java is written without dealing with the lower level semantics often associated with procedural programming it still supports the principles of procedural programming.

## Functional Programming
Java supports the use of lambdas, anonymous inner classes, and functional interfaces so it therefore supports functional programming.

## Multithreading
#### Threads or thread-like abilities
Java can implement theads by either extending the Thread class or implementing the Runnable interface. Both of these ways provide a class with the functionality of a thread. The code implemented during the runtime of a thread goes within its run() method and begins when the classes start() method is called.
#### How is multitasking accomplished?
Java is a multithreaded language meaning it is capable of handling multiple threads running at once. To do so, seperate threads must simple be running at the same time and the two threads will alternate execution while operating concurrently.
