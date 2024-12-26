
## OOPS Day 5

**Topics Covered**
--------------
1. [instanceof Operator](#1-instanceof-operator)
2. [Cloning](#2-cloning)
    - [Shallow Cloning](#21-shallow-cloning)
    - [Deep Cloning](#22-deep-cloning)
3. [Immutable Class](#3-immutable-class)
    - [Custom Immutable](#31-custom-immutable)
    - [Scenario where Immutability of Class can Break](#32-scenario-where-immutability-of-class-can-break)
    - [Protecting Immutability of Immutable Class](#33-protecting-immutability-of-immutable-class)
4. [Nested Class](#4-nested-class)
    - [Static Nested Class](#41-static-nested-class)
    - [Instance Nested Class](#42-instance-nested-class)
    - [Local Inner Class](#43-local-inner-class)
    - [Anonymous Class](#44-anonymous-class)
--------------

## 1. instanceof Operator

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instanceof-video">
             <img src="https://img.youtube.com/vi/link-to-instanceof-video/0.jpg" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">1. instanceof Operator</th>
    </tr>
</table>

The `instanceof` operator is used to check whether an object is an instance of a specific class or interface, allowing for type checking and type conversion in Java.

```java
Child child = new Child();
System.out.println(child instanceof Child); // true

Parent parent = new Child();
System.out.println(parent instanceof Child); // true
```

## 2. Cloning

### 2.1 Shallow Cloning

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-shallow-cloning-video">
             <img src="https://img.youtube.com/vi/link-to-shallow-cloning-video/0.jpg" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">2.1 Shallow Cloning</th>
    </tr>
</table>

Shallow cloning creates a new object but copies the references of the original object's fields, not the actual objects.

### 2.2 Deep Cloning

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-deep-cloning-video">
             <img src="https://img.youtube.com/vi/link-to-deep-cloning-video/0.jpg" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">2.2 Deep Cloning</th>
    </tr>
</table>

Deep cloning creates a new object and also creates new copies of the objects referenced by the original object's fields.

## 3. Immutable Class

### 3.1 Custom Immutable

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-custom-immutable-video">
             <img src="https://img.youtube.com/vi/link-to-custom-immutable-video/0.jpg" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">3.1 Custom Immutable</th>
    </tr>
</table>

An immutable class is a class whose instances cannot be modified once created.

### 3.2 Scenario where Immutability of Class can Break

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-immutability-break-video">
             <img src="https://img.youtube.com/vi/link-to-immutability-break-video/0.jpg" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">3.2 Scenario where Immutability of Class can Break</th>
    </tr>
</table>

Certain conditions and improper handling can cause the immutability of a class to break.

### 3.3 Protecting Immutability of Immutable Class

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-protecting-immutability-video">
             <img src="https://img.youtube.com/vi/link-to-protecting-immutability-video/0.jpg" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">3.3 Protecting Immutability of Immutable Class</th>
    </tr>
</table>

Proper techniques and practices can help ensure the immutability of a class.

## 4. Nested Class

### 4.1 Static Nested Class

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-static-nested-class-video">
             <img src="https://img.youtube.com/vi/link-to-static-nested-class-video/0.jpg" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">4.1 Static Nested Class</th>
    </tr>
</table>

A static nested class is defined within another class but cannot access the non-static members of the outer class.

### 4.2 Instance Nested Class

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instance-nested-class-video">
             <img src="https://img.youtube.com/vi/link-to-instance-nested-class-video/0.jpg" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">4.2 Instance Nested Class</th>
    </tr>
</table>

An instance nested class, also known as an inner class, can access both static and non-static members of the outer class.

### 4.3 Local Inner Class

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-local-inner-class-video">
             <img src="https://img.youtube.com/vi/link-to-local-inner-class-video/0.jpg" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">4.3 Local Inner Class</th>
    </tr>
</table>

A local inner class is defined within a block such as a method or a loop and can access the local variables of that block.

### 4.4 Anonymous Class

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-anonymous-class-video">
             <img src="https://img.youtube.com/vi/link-to-anonymous-class-video/0.jpg" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">4.4 Anonymous Class</th>
    </tr>
</table>

An anonymous class is a class without a name and is defined and instantiated in a single expression.
