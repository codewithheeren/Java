## OOPS Day 1
<span style="color:blue">some *blue* text</span>.
 @author Heeren

 **Topics Covered**
--------------
1. [Java Features and Compilation, Execution Architecture of Java Program](#1-java-features-and-compilation-execution-architecture-of-java-program)       
2. [Types of Class Loaders and Java Development Kit (JDK)](#types-of-class-loaders-and-java-development-kit-jdk)         
3. [Variables and Data Types](#13-variables-and-data-types)    
4. [Classification of Data Types](#14-classification-of-data-types)    
5. [Naming Conventions of Variables](#15-naming-conventions-of-variables)    
6. [OOPs (Object-Oriented Programming)](#16-oops-object-oriented-programming)    
    - [Object](#object)    
    - [Class](#class)    
    - [Static Variable](#static-variable)    
    - [Instance Variable](#instance-variable)    
    - [Static Method](#static-method)    
    - [Instance Method](#instance-method)   
    - [Local Variable](#local-variable)    
    - [Data Shadowing](#data-shadowing)    
    - [**this** Keyword](#this-keyword)    
    - [Data Hiding **Super** keyword](#data-hiding-super-keyword)    
    
--------------

## 1. Java Features and Compilation, Execution Architecture of Java Program
 
<table>
    <tr>
        <td><a href="https://www.youtube.com/watch?v=example1">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th>1.1 Platform independent language</th>
    </tr>
 </table> 
 
🔵 **Plateform Dependency With C Language Program**  

![c prgram](https://github.com/codewithheeren/Java/assets/87074236/450da9f3-99c5-4cd6-bf8c-dab36ad42986)      


🔵 **Plateform Independency with Java Program Execution**

Java Program -> **javac Compiler** -> Byte Code ->** JRE **-> Machine Code

![image](https://github.com/user-attachments/assets/989499d5-d72a-4c95-9e4e-7d0c1e611218)
 <table>
    <tr>
        <td><a href="https://www.youtube.com/watch?v=example1">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th>1.2 Secure language</th>
    </tr>
    <tr>
        <td><a href="https://www.youtube.com/watch?v=example1">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th>1.3 Robust language</th>
    </tr>
  </table>
  
  🔵 **Compilation And Execution Architecture of A Java Program**
  ![image](https://github.com/codewithheeren/Java/assets/87074236/759457a2-bd58-4fa3-9fe4-09d68f969826)
  
  <table>
    <tr>
        <td><a href="https://www.youtube.com/watch?v=example1">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th>1.4 Multithreaded language</th>
    </tr>
   <tr>
        <td><a href="https://www.youtube.com/watch?v=example1">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th>1.5 Object oriented language</th>
    </tr>
    <tr>
        <td><a href="https://www.youtube.com/watch?v=example1">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th>1.6 Open source language</th>
    </tr>
</table>

---
## Types of Class Loaders and Java Development Kit (JDK)
<table>
<tr>
        <td><a href="https://www.youtube.com/watch?v=example1">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th>2. Types of Class Loaders and Java Development Kit</th>
    </tr>
</table>

🔵 **Types of Class Loaders**

1. Bootstrap class loader - loads all the JAR files (placed inside **rt.jar**)
2. Extension class loader
3. Application class loader
   
🔵 **JDK Vesions and Components**
- Java SE 7 (July 28, 2011)
- Java SE 8 (March 18, 2014)
- Java SE 9 (September 21, 2017)
- Java SE 10 (March 20, 2018)
- Java SE 11 (September 25, 2018)
- Java SE 12 (March 19, 2019)
- Java SE 13 (September 17, 2019)
- Java SE 14 (March 17, 2020)
- Java SE 15 (September 15, 2020)
- Java SE 16 (March 16, 2021)
- Java SE 17 (September 14, 2021)

🔵 **Java Installation**    
[Download JDK1.8](https://drive.google.com/uc?export=download&id=1IIZAzCiDsJe6nGhAcnJOmVpDnMiu8MqV)

**JDK -> JDK + JRE**

---

**Variables and DataTypes**   
**characteristics of Variables**
- Must not start from a number.
- No two variables with the same name are allowed in the same function.
- Variable must be declared before its first use.
- Variable names must not be a keyword.
- Space is not allowed.
- Same type variables can be declared using a comma.
- Variable name must be meaningful and must not contain any operator.
---
**Classification of Data Types**

![image](https://github.com/codewithheeren/Java/assets/87074236/36f43577-4fcc-400a-b6f2-1e9d7d8957f7)

---

**Hello World Java Program - Conventions **
- Class Name Convention: First letter capital (camel case for variables and methods, capitals for final variables)

- File Should Contain One Class Only

**File Name: DemoOfJava.java**
```java
class DemoOfJava {
    public static void main(String[] args) {
        System.out.println("Hello Java.");
    }
}
```
---

**OOPS (Object Oriented Programming)**
- Object
- Class
- Class Members
- Methods
- Variables / Class Data Members
- Classification of Data Members and Methods
- Static and Instance
- Static Variables
- Instance Variables

---

**Local Variable**     
A local variable in Java is a variable declared inside a method, constructor, or block. It is only accessible within that scope and is created when the method, constructor, or block is executed, and destroyed once it finishes. Local variables are stored in the stack memory.

---

**Data Shadowing and Data Hiding**    
If method's local variable and class level variable having same name then inside the method local priority will goes to method's local variable. That is known as data shadowing.In this case 'this' Keyword is use to access class level variable.    
    
In case of Inheritance if parent class data member and child class data memeber having same name then from child class priority will goes to child class data member, that is known as data hiding.  In this case 'super' keyword is use to access parent class variable.

---
