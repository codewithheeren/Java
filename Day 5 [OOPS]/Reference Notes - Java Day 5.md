
## OOPS Day 5

**Topics Covered**
--------------
**Topics Covered**
--------------
1. [instanceof Operator](#1-instanceof-operator)
2. [Cloning](#2-cloning)
    - Shallow Cloning
    - Deep Cloning
3. [Immutable Class](#3-immutable-class)
    - Custom Immutable
    - Scenario where Immutability of Class can Break
    - Protecting Immutability of Immutable Class
4. [Nested Class](#4-nested-class)
    - Static Nested Class
    - Instance Nested Class
    - Local Inner Class
    - Anonymous Class
    - Inner Interface
--------------

## 1. instanceof Operator

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instanceof-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">1. instanceof Operator</th>
    </tr>
</table>

🔵 The `instanceof` operator is used to check whether an object is an instance of a specific class or interface, allowing for type checking and type conversion in Java.    

`Child child = new Child();`     
`sysout(child instanceof Child) ->   true`     
   
`Parent parent = new Child();`    
`sysout(parent instanceof Child) ->   true`   

## 2. Cloning

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-shallow-cloning-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">2.1 Cloning</th>
    </tr>
</table>


<table>
    <tr>
        <td><a href="https://youtu.be/link-to-deep-cloning-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">2.2 Shallow Cloning And Deep Cloning</th>
    </tr>
</table>

🔵 Shallow cloning creates a new object but copies the references of the original object's fields, not the actual objects.

🔵 Deep cloning creates a new object and also creates new copies of the objects referenced by the original object's fields.

## 3. Immutable Class
An immutable class is a class whose instances cannot be modified once created.
<table>
    <tr>
        <td><a href="https://youtu.be/link-to-custom-immutable-video">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">3. Immutable Class</th>
    </tr>
</table>

🔵 **Custom Immutable Class Creation**
Following rules need to follow in order to create custom immutable class -              
 * Class must be final.     
 * Class data members must be private and final.    
 * Do not define any setter method in that class.   
 * Data members must initialize using constructor only.    

🔵**Scenario where Immutability of Class can Break**   
🔵**Protecting Immutability of Immutable Class**   


## 4. Nested Class
A nested class, also known as an inner class, is a class declared inside another class or interface. Inner classes are used to logically group classes and interfaces in one place for improved readability and maintainability. They can access all members of the outer class, including private data members and methods.

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-static-nested-class-video">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">4.1 Static Nested Class</th>
    </tr>
</table>

- A class that is created inside a class, is called a static nested class in Java. It cannot access non-static data members and methods. 
- It can be accessed by outer class name.
- It can access static data members of the outer class, including private.
- Static nested class cannot access non-static (instance) data members of outer class .

🔵 **What Happens with nested class at Compile Time?**

When a program containing a local inner class is compiled, the compiler generates two .class files:

- Outer.class
- Outer$1Inner.class

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instance-nested-class-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">4.2 Instance Nested Class</th>
    </tr>
</table>

- An instance nested class can access both static and non-static (instance) members of the outer class.    
- It can only have instance data member inside it.     
- Instance nested class only access by using inner class object reference.     
- Data Shadowing in Inner Class.    

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-local-inner-class-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">4.3 Local Inner Class</th>
    </tr>
</table>

- Local inner classes are defined inside a block, which can be a method body, a for loop, or an if clause. 
- Accessing within the Instance method: Can access all data members.    
- Defined in a static method: Can access all static members.    
- Can not modify local variable of method, because by default that will treat as final variable.    

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-anonymous-class-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">4.4 Anonymous Class</th>
    </tr>
</table>

- An anonymous inner class is a class without a name, known as an anonymous class. 
- It is always represented by its parent (class or interface) name. 
- An anonymous class is created and instantiated in the same step and does not contain any explicit constructor due to its lack of a name.

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-anonymous-class-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">4.5 Inner Interface</th>
    </tr>
</table>

- Declaration of an inner interface occurs in the body of another interface or class.       
- If declared in another class, it must be `static` but can have any access modifier.        
- If declared in another interface, it must be `static` and `public`.        
