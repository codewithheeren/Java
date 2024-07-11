## OOPS Day 1

 @author Heeren

 **Topics Covered**
--------------
1.1   Features of Java
1.2   Compilation and Execution Architecture of Java Program
1.3   Types of Class Loaders
1.4   Variables and Data Types
1.5   Classification of Data Types
1.6   Naming Conventions of Variables
1.7   OOPs (Object-Oriented Programming)
    -   Object
    -   Class
    -   Static Variable
    -   Instance Variable
    -   Static Method
    -   Instance Method
    -   Local Variable
    -   Data Shadowing
    -   **this** Keyword
    -   Data Hiding **Super** keyword
    
--------------

**Features of Java**

- Platform independent language
- Secure language
- Robust language
- Multithreaded language
- Object oriented language
- Open source language

---

**C Program**


![c prgram](https://github.com/codewithheeren/Java/assets/87074236/450da9f3-99c5-4cd6-bf8c-dab36ad42986)      


---

**Java Program**

Java Program -> **javac Compiler** -> Byte Code ->** JRE **-> Machine Code

---

**JDK Vestions and Components**
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

**JDK -> JDK + JRE**

---

**Types of Class Loaders**

1. Bootstrap class loader - loads all the JAR files (placed inside **rt.jar**)
2. Extension class loader
3. Application class loader

![image](https://github.com/codewithheeren/Java/assets/87074236/759457a2-bd58-4fa3-9fe4-09d68f969826)

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
