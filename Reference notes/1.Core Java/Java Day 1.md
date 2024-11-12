## OOPS Day 1
@author Heeren

 **Topics Covered**
--------------
1. [Java Features and Compilation, Execution Architecture of Java Program](#1-java-features-and-compilation-execution-architecture-of-java-program)       
2. [Types of Class Loaders](#2-types-of-class-loaders)       
3. [Variables and Data Types](#3-variables-and-data-types)
4. [IDE and JDK Installation](#4-ide-and-jdk-installation)
5. [First Java Program](#4-first-java-program)      
6. [OOPS Fundamentals](#5-oops-fundamentals)
7. [Data Shadowing and Data Hiding](#6-data-shadowing-and-data-hiding)  
--------------

## 1. Java Features and Compilation, Execution Architecture of Java Program
 
<table>
    <tr>
        <td><a href="https://www.youtube.com/watch?v=SUnAsQykPfw&list=PLI8XC2Oz_l1qMnpB-6Kc3Ck0RuCqDKCCQ&index=1">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">1.1 Platform independent language</th>
    </tr>
 </table> 
 
🔵 **Plateform Dependency With C Language Program**  

![c prgram](https://github.com/codewithheeren/Java/assets/87074236/450da9f3-99c5-4cd6-bf8c-dab36ad42986)      


🔵 **Plateform Independency with Java Program Execution**

Java Program -> **javac Compiler** -> Byte Code ->** JRE **-> Machine Code

![image](https://github.com/user-attachments/assets/989499d5-d72a-4c95-9e4e-7d0c1e611218)
 <table>
    <tr>
        <td><a href="https://www.youtube.com/watch?v=1xjKbfvh01o&list=PLI8XC2Oz_l1qMnpB-6Kc3Ck0RuCqDKCCQ&index=2">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">1.2 Secure language</th>
    </tr>
    <tr>
        <td><a href="https://www.youtube.com/watch?v=1xjKbfvh01o&list=PLI8XC2Oz_l1qMnpB-6Kc3Ck0RuCqDKCCQ&index=2">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">1.3 Robust language</th>
    </tr>
  </table>
  
  🔵 **Compilation And Execution Architecture of A Java Program**
  ![image](https://github.com/codewithheeren/Java/assets/87074236/759457a2-bd58-4fa3-9fe4-09d68f969826)
  
  <table>
    <tr>
        <td><a href="https://www.youtube.com/watch?v=GB7Hiem95zc&list=PLI8XC2Oz_l1qMnpB-6Kc3Ck0RuCqDKCCQ&index=3">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">1.4 Multithreaded language</th>
    </tr>
   <tr>
        <td><a href="https://www.youtube.com/watch?v=GB7Hiem95zc&list=PLI8XC2Oz_l1qMnpB-6Kc3Ck0RuCqDKCCQ&index=3">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">1.5 Object oriented language</th>
    </tr>
    <tr>
        <td><a href="https://www.youtube.com/watch?v=kNukMHUg9Ew&list=PLI8XC2Oz_l1qMnpB-6Kc3Ck0RuCqDKCCQ&index=4">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">1.6 Open source language</th>
    </tr>
</table>

---
## 2. Types of Class Loaders
<table>
<tr>
        <td><a href="https://www.youtube.com/watch?v=example1">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">2. Types of Class Loaders and Java Development Kit</th>
    </tr>
</table>

🔵 **Types of Class Loaders**

1. Bootstrap class loader - loads all the JAR files (placed inside **rt.jar**)
2. Extension class loader
3. Application class loader
---
## 3. Variables and Data Types

 <table>
    <tr>
        <td><a href="https://www.youtube.com/watch?v=WkClbsavfro&list=PLI8XC2Oz_l1qMnpB-6Kc3Ck0RuCqDKCCQ&index=5">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">3.1 Variables and DataTypes</th>
    </tr>
 </table>
 
🔵 **Variable** 
A variable is a named storage location in memory that holds a value.   
🔵 **Data Type**
A data type defines the type of value a variable can store, such as integers, floating-point numbers, or text.       
  <table>
   <tr>
        <td><a href="https://www.youtube.com/watch?v=example1">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">3.2 Characteristics of Variables</th>
    </tr>
</table>

- Must not start from a number.     
- No two variables with the same name are allowed in the same function.   
- Variable must be declared before its first use.   
- Variable names must not be a keyword.    
- Space is not allowed.   
- Same type variables can be declared using a comma.    
- Variable name must be meaningful and must not contain any operator.   

<table>
   <tr>
        <td><a href="https://www.youtube.com/watch?v=example1">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">3.3 Classification of Data Types</th>
    </tr>
</table>

![image](https://github.com/codewithheeren/Java/assets/87074236/36f43577-4fcc-400a-b6f2-1e9d7d8957f7)

---
## 4. IDE and JDK Installation  
<table>
<tr>
        <td><a href="https://www.youtube.com/watch?v=qlxOjEtEJmc&list=PLI8XC2Oz_l1qMnpB-6Kc3Ck0RuCqDKCCQ&index=7&t=18s">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">4. Java Environment Setup</th>
    </tr>
</table>

🔵 **JDK (Java Development Kit) Major Vesions**      
- JDK 1.5 (Java 5) Release Date: September 30, 2004  
- JDK 1.6 (Java 6) Release Date: December 11, 2006  
- JDK 1.7 (Java 7) Release Date: July 28, 2011  
- JDK 1.8 (Java 8) Release Date: March 18, 2014  
- JDK 9 Release Date: September 21, 2017   
- JDK 10 Release Date: March 20, 2018   
- JDK 11 (LTS) Release Date: September 25, 2018   
- JDK 17 (LTS) Release Date: September 14, 2021   

🔵 **Java Installation**    

[Download JDK1.8](https://drive.google.com/uc?export=download&id=1IIZAzCiDsJe6nGhAcnJOmVpDnMiu8MqV)

**JDK -> JDK + JRE**

🔵 **STS / Eclipse Installation**    

[Download STS](https://drive.google.com/file/d/1Fp5q_-em70fZ4hR0FACOVuZWhLJj0l2l/view?usp=drive_link)   
[Download Eclipse](https://drive.google.com/file/d/1U_ikAcubg0l_UgPIFMKA-r4kCIzoROYp/view?usp=sharing)

---
## 5. First Java Program
<table>
    <tr>
        <td><a href="https://www.youtube.com/watch?v=example1">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">4. First Java Program</th>
    </tr>
 </table>
 
**DemoOfJava.java**
```java
class DemoOfJava {
    public static void main(String[] args) {
        System.out.println("Hello Java.");
    }
}
```
🔵 **Conventions**
- First letter of class name for each word must be capital (camel case for variables and methods, capitals for final variables).
- One java file should contain one class only.
---
## 6. OOPS Fundamentals
<table>
    <tr>
        <td><a href="https://www.youtube.com/watch?v=example1">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">5. OOPS fundamentals</th>
    </tr>
 </table>
 
🔵 **6.1 Object, Class and Class Members**
- Object
- Class
- Class Members
    - Methods
    - Variables / Data Members
- Classification of Data Members and Methods
    
🔵 **6.2 Static and Instance**
- Static Variables
- Instance Variables
- Static Method
- Instance Method     
🔵 **6.3 Local Variable**     
A local variable in Java is a variable declared inside a method, constructor, or block. It is only accessible within that scope and is created when the method, constructor, or block is executed, and destroyed once it finishes. Local variables are stored in the stack memory.
---
## 7. Data Shadowing and Data Hiding
<table>
    <tr>
        <td><a href="https://www.youtube.com/watch?v=example1">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">6. Data Shadowing and Data Hiding</th>
    </tr>
 </table>
 
🔵 **Data Shadowing**    
If method's local variable and class level variable having same name then inside the method local priority will goes to method's local variable. That is known as data shadowing.In this case 'this' Keyword is use to access class level variable. 

🔵 **Data Hiding**   
In case of Inheritance if parent class data member and child class data memeber having same name then from child class priority will goes to child class data member, that is known as data hiding.  In this case 'super' keyword is use to access parent class variable.

---
