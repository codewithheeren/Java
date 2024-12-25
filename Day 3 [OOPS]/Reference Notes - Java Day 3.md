## OOPS Day 3
**Topics Covered**
--------------
1. [Constructor](#1-constructor)
2. [Instance block / Init block And Constructor Overloading](#2-instance-block--init-block-and-Constructor-Overloading)
3. [Constructor chaining](#3-constructor-chaining)
4. [Anonymous object](#4-anonymous-object)
5. [Static block](#5-static-block)
6. [final keyword](#6-final-keyword)
7. [Call by value and call by reference](#7-call-by-value-and-call-by-reference)
8. [Packages, default package, import, and package keyword](#8-packages-default-package-import-and-static-Import)
9. [Assignment](#9-assignment)
--------------

## 1. Constructor

<table>
    <tr>
        <td><a href="https://youtu.be/Tb5FfNaStgI">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">1.1 Constructor  And Object creation using 'new' Keyword</th>
    </tr>
</table>

Constructor is a special member function of the class.
- Having same name as class name.
- We do not define return type for constructor.
- Constructor can not explicitly call.

🔵 **New keyword**  

The new keyword in Java is used to create an instance of a class. When **new** is used:   
- It allocates memory at runtime in the heap area.
- **new** invokes the class constructor to initialize the newly created object.

<table>
    <tr>
        <td><a href="https://www.youtube.com/watch?v=MHlG7pW8z3s">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">1.2 Constructor classification and object initialization</th>
    </tr>
</table>

Constructor overloading refers to having multiple constructors within a class, each with a different set of parameters.

🔵 **Default Constructor**   
A constructor with no arguments provided explicitly.   

🔵 **Non Parameterize Constructor**   
A constructor without any parameters.    

🔵 **Parameterize Constructor**    
A constructor that accepts parameters to initialize the object.   

---
## 2. Instance block / Init block And Constructor Overloading

<table>
    <tr>
        <td><a href="https://www.youtube.com/watch?v=sY0u4sg0NCA">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">2. Instance block</th>
    </tr>
</table>   

🔵 **Constructor Overloading**
More then one costructors in same class with different paramaters is known as constructor overloading.  

🔵 **Instance block**
Instance blocks are name-less block in Java that possess common logic for all constructors.

---
## 3. Constructor chaining

<table>
    <tr>
        <td><a href="https://youtu.be/zdgvBmDK8hA">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">3. Constructor chaining</th>
    </tr>
</table>

Constructor chaining refers to one constructor calling another constructor within the same class or in a superclass.  

🔵 **Constructor chaining in same class**   
🔵 **Constructor chaining in parent class**   
🔵 **Constructor never become the part of inheritance. Why?**   

---
## 4. Anonymous object

<table>
    <tr>
        <td><a href="https://youtu.be/8hM6QqVw3SU">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">4. Anonymous object</th>
    </tr>
</table>

An anonymous object in Java refers to an object without a name that is created and used only once.

---
## 5. Static block

<table>
    <tr>
        <td><a href="https://youtu.be/CGGkIliWdh4">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">5. Static block</th>
    </tr>
</table>

A static block in Java is used to initialize static data members dynamically:
- Static block execute before the main method.
- Static block executed only once.
- Static block executed in sequential order.

---
## 6. final keyword

<table>
    <tr>
        <td><a href="https://youtu.be/euZJVGamX8M">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">6. final keyword</th>
    </tr>
</table>

The `final` keyword is used to declare constants and prevent inheritance and overriding.

---
## 7. Call by value and call by reference

<table>
    <tr>
        <td><a href="#">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">7. Call by value and call by reference</th>
    </tr>
</table>

Java supports call by value where a copy of the value is passed, and modifications are not reflected outside the method.

---
## 8. Packages, default package, import and static Import

<table>
    <tr>
        <td><a href="#">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">8. Packages, default package, import and static Import</th>
    </tr>
</table>

🔵 **package**  
Packages in Java are used to group related classes and interfaces together, providing a namespace for managing class and interface names.     
🔵 **import**     
import keyword is use to import one package into another package.    
🔵 **import static**  
Static import in Java allows members (fields and methods) defined in a class to be used in Java code without specifying the class.   
🔵 **Advantage of Static Import**
Requires less coding if you frequently access static members of a class.

---
## 9. Assignment      
**Task 1: Develop Secure Online Shopping System, implement following requirements-**       
🔵 Classes and Constructors: Create Product and ShoppingCart classes. Product should have properties like ID, name, and price with parameterized constructors.      
🔵 Anonymous Object: Use anonymous objects to add products to the shopping cart.      
🔵 final Keyword: Make Product properties final to ensure immutability.      

**Task 2: Develop Banking System with Immutable Transactions, implement following requirements-**           
🔵 Classes and Constructors: Create BankAccount and Transaction classes. BankAccount should include properties like account number, holder name, and balance and Transaction can include transactionID, amount, timestamp.     
🔵 Constructor Chaining: Implement constructor chaining within BankAccount.    
🔵 Instance Block: Use an instance block to print a message upon account creation.     
🔵 final Keyword: Make Transaction properties final and ensure the class is immutable.     

**Task 3: School System with Inheritance and Constructor Chaining, implement following requirements-**       
🔵 Classes and Constructors: Create a base class Person and a derived class Student.     
🔵 Constructor Chaining: Use constructor chaining to initialize Person and Student properties.     
🔵 Instance Block: Add an instance block in Student to print a message upon student creation.      

**Task 4. Build a Configurable Application with Static Imports, implement following requirements-**    
🔵 Configuration Loader: Create a ConfigLoader class with a static block to load settings from a properties file.    
🔵 Static Import: Use static import in another class AppSettings to access configuration settings without class name.  

**Task 5: Build an Inventory Management System with Call by Reference Simulation, implement following requirements-**    
🔵 Classes and Constructors: Create Item class with properties like item ID and quantity.       
🔵 Call by Value and Call by Reference: Implement a method swapItems to swap properties of Item objects simulating call by reference.     


