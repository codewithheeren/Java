## OOPS Day 3

 @author Heeren

 **Topics Covered**
--------------
-   Covariant type method overriding
-   Method Hiding
-   New keyword
-   Constructor
    -   Default Constructor
    -   Non Parameterize Constructor
    -   Parameterize Constructor
-   Types of Constructor
-   Instance block 
-   Constructor chaining
    -   Constructor chaining in same class
    -   Constructor chaining in parent class
-   Constructor never become the part of inheritance
-   Annonymous object 
-   Static block 
-   final keyword
-   Call by value and call by reference 
-   Packages , default package ,import and package keyword 
-   static Import  
--------------
**New Keyword**

The new keyword in Java is used to create an instance of a class. When **new** is used:
-   It allocates memory at runtime in the heap area.
-   **new** invokes the class constructor to initialize the newly created object.

---
**Constructor**   
Constructor is a special memeber function of the class.
-   Having same name as class name.
-   We do not define return type for constructor.
-   Constructor can not explicitly call.
  
**Type of Constructors**   

**Parameterized Constructor**

A constructor that accepts parameters to initialize the object.

**Non-Parameterized Constructor**

A constructor without any parameters.

**Default Constructor**

A constructor with no arguments provided explicitly.

**Constructor Overloading**   

Constructor overloading refers to having multiple constructors within a class, each with a different set of parameters.

-   Default Constructor (No-Arg Constructor)
-   Parameterized Constructor

---
**Instance Block / Init Block**   
Instance blocks are name-less block in Java that possess common logic for all constructors .

---   
**Constructor Chaining**    
Constructor chaining refers to one constructor calling another constructor within the same class or in a superclass.   

---
**Static Block**   
A static block in Java is used to initialize static data members dynamically:
-   Static blocks are executed just after class loading by the JVM.
-   They are executed just before the execution of the `main` method.
-   Static blocks are used for static initialization tasks.
  
---
**Anonymous Object**   
An anonymous object in Java refers to an object without a name that is created and used only once.

---   
**Final Keyword**    
The `final` keyword in Java can be used on variables, classes, or methods:

-   A `final` class cannot be inherited.
-   A `final` method cannot be overridden.
-   A `final` variable's value cannot be changed once assigned.

**Blank Final Static**    
A blank final static variable is a final variable that is not initialized during declaration. Values must be assigned in the constructor.

---    
**Package**    
A package is a group of similar types of classes, interfaces, and sub-packages. In Java, packages can be categorized into two forms: built-in packages and user-defined packages.

**How to Access a Package from Another Package?**   
**Using packagename.**     
import package.*;   
**Using packagename.classname**     
import package.classname;   
**Using fully qualified name**   
packagename.classname obj = new packagename.classname();

**Default Package**  
The `java.lang` package is a default package in Java.

**Static Import**  
The static import feature introduced in Java 5 allows Java programmers to access any static member of a class directly without qualifying it with the class name.

**Advantage of Static Import**  
-   Requires less coding if you frequently access static members of a class.


