## OOPS Day 3
**Topics Covered**
--------------
1. [Constructor](#1-constructor)
2. [Types of Constructor](#2-types-of-constructor)
3. [Instance block](#3-instance-block)
4. [Constructor chaining](#4-constructor-chaining)
    - [Constructor chaining in same class](#constructor-chaining-in-same-class)
    - [Constructor chaining in parent class](#constructor-chaining-in-parent-class)
5. [Constructor never become the part of inheritance](#5-constructor-never-become-the-part-of-inheritance)
6. [Anonymous object](#6-anonymous-object)
7. [Static block](#7-static-block)
8. [final keyword](#8-final-keyword)
9. [Call by value and call by reference](#9-call-by-value-and-call-by-reference)
10. [Packages, default package, import, and package keyword](#10-packages-default-package-import-and-package-keyword)
11. [static Import](#11-static-import)
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

## 2 Types of Constructor

<table>
    <tr>
        <td><a href="#">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">2.1 Types of Constructor</th>
    </tr>
</table>

Constructor overloading refers to having multiple constructors within a class, each with a different set of parameters.

- Default Constructor (No-Arg Constructor)
- Parameterized Constructor


### 2.1 Default Constructor

<table>
    <tr>
        <td><a href="#">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">2.2 Default Constructor</th>
    </tr>
</table>

A constructor with no arguments provided explicitly.

### 2.3 Non Parameterize Constructor

<table>
    <tr>
        <td><a href="#">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">2.3 Non Parameterize Constructor</th>
    </tr>
</table>

A constructor without any parameters.

### 1.4 Parameterize Constructor

<table>
    <tr>
        <td><a href="#">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">1.4 Parameterize Constructor</th>
    </tr>
</table>

A constructor that accepts parameters to initialize the object.

---
## 3. Instance block

<table>
    <tr>
        <td><a href="#">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">3. Instance block</th>
    </tr>
</table>

Instance blocks are name-less block in Java that possess common logic for all constructors.

## 4. Constructor chaining

<table>
    <tr>
        <td><a href="#">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">4. Constructor chaining</th>
    </tr>
</table>

Constructor chaining refers to one constructor calling another constructor within the same class or in a superclass.

### 4.1 Constructor chaining in same class

<table>
    <tr>
        <td><a href="#">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">4.1 Constructor chaining in same class</th>
    </tr>
</table>

### 4.2 Constructor chaining in parent class

<table>
    <tr>
        <td><a href="#">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">4.2 Constructor chaining in parent class</th>
    </tr>
</table>

## 5. Constructor never become the part of inheritance

<table>
    <tr>
        <td><a href="#">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">5. Constructor never become the part of inheritance</th>
    </tr>
</table>

## 6. Anonymous object

<table>
    <tr>
        <td><a href="#">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">6. Anonymous object</th>
    </tr>
</table>

An anonymous object in Java refers to an object without a name that is created and used only once.

## 7. Static block

<table>
    <tr>
        <td><a href="#">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">7. Static block</th>
    </tr>
</table>

A static block in Java is used to initialize static data members dynamically:
- Static block execute before the main method.
- Static block executed only once.
- Static block executed in sequential order.

## 8. final keyword

<table>
    <tr>
        <td><a href="#">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">8. final keyword</th>
    </tr>
</table>

The `final` keyword is used to declare constants and prevent inheritance and overriding.

## 9. Call by value and call by reference

<table>
    <tr>
        <td><a href="#">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">9. Call by value and call by reference</th>
    </tr>
</table>

Java supports call by value where a copy of the value is passed, and modifications are not reflected outside the method.

## 10. Packages, default package, import, and package keyword

<table>
    <tr>
        <td><a href="#">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">10. Packages, default package, import, and package keyword</th>
    </tr>
</table>

Packages in Java are used to group related classes and interfaces together, providing a namespace for managing class and interface names.

## 11. static Import

<table>
    <tr>
        <td><a href="#">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">11. static Import</th>
    </tr>
</table>

Static import in Java allows members (fields and methods) defined in a class to be used in Java code without specifying the class.

**Advantage of Static Import**
Requires less coding if you frequently access static members of a class.
