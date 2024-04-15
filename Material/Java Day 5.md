## OOPS Day 5

 @author Heeren

 **Topics Covered**
--------------
- instanceof operator
- Cloning
  - Shallow cloning 
  - Deep cloning 
- Immutable class
- Nested Class
    - Static nested
    - Instance nested class
    - Local inner class
    - Anonymous class
--------------
## instanceof Operator

The `instanceof` operator is used to check whether an object is an instance of a specific class or interface, allowing for type checking and type conversion in Java.
Child child = new Child();
sysout(child instance of Child) ->   true   
   
Parent parent = new Child();   
sysout(parent instance of Child) ->   true

###  Nested Class or Inner Class: What and Why?

A nested class, also known as an inner class, is a class declared inside another class or interface. Inner classes are used to logically group classes and interfaces in one place for improved readability and maintainability. They can access all members of the outer class, including private data members and methods.

### Static Nested Class

- A class that is created inside a class, is called a static nested class in Java. It cannot access non-static data members and methods. 
- It can be accessed by outer class name.
- It can access static data members of the outer class, including private.
Th- e static nested class cannot access non-static (instance) data members of outer class .


### Instance Nested Class / Inner class

- An instance nested class can access both static and non-static (instance) members of the outer class.
- It can only have instance data member inside it.
- Instance nested class only access by using inner class object reference.
- Data Shadowing in Inner Class

### Local Inner Class

- Local inner classes are defined inside a block, which can be a method body, a for loop, or an if clause.
- Accessing within the Instance method: Can access all data members.
- Defined in a static method: Can access all static members.
- Can not modify local variable of method, because by default that will treat as final variable.

**What Happens at Compile Time?**

When a program containing a local inner class is compiled, the compiler generates two .class files:

- Outer.class
- Outer$1Inner.class

**Anonymous Inner Class**

- An anonymous inner class is a class without a name, known as an anonymous class. 
- It is always represented by its parent (class or interface) name. 
- An anonymous class is created and instantiated in the same step and does not contain any explicit constructor due to its lack of a name.



