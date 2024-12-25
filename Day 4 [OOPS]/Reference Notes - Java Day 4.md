## OOPS Day 4

**Topics Covered**
--------------
1. [Abstraction And Interfaces](#1-abstraction-and-interfaces)
2. [Abstract Class And Difference b/w Abstract Class and Interface](#2-abstract-class-and-difference-bw-abstract-class-and-interface)
3. [Marker Interface And Inner Interface](#3-marker-interface-and-inner-interface)
4. [Encapsulation](#4-encapsulation)
5. [Type Casting](#5-type-casting)
6. [Object class](#6-object-class)
7. [Equality vs equals method](#7-equality-vs-equals-method)
8. [ToString method](#8-tostring-method)
--------------
  
## 1. Abstraction And Interfaces

<table>
    <tr>
        <td><a href="#">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">1. Abstraction And Interfaces </th>
    </tr>
</table>

🔵 **Abstraction**    
Abstraction is the process of showing functionality while hiding the implementation. It can be achieved in Java using interfaces or abstract classes.abstraction is use to achive generalization.

![interface](https://github.com/codewithheeren/Java/assets/87074236/47c765b2-26ff-47c4-91d0-d7d267522525)  

🔵 **Interface**
- Blueprint of a class.
- Methods defined in interfaces are by default public and abstract.
- Interface data members are by default public, static, and final.
- Objects cannot be created from an interface.
- No constructor can be defined in an interface.
- When a class implements an interface, it needs to override all methods.
- Java supports multiple inheritance through interfaces (a class can implement multiple interfaces).
  
🔵 **Abstract Method**   
- Method without a body.     
- Defined using the `abstract` keyword.     
- Cannot be defined inside a concrete or normal class.     
- Used in interfaces and abstract classes.  

## 2. Abstract Class And Difference b/w Abstract Class and Interface  
<table>
    <tr>
        <td><a href="#">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">2. Abstract Class And Abstract Class vs Interface</th>
    </tr>
</table>

🔵 **Abstract Class**
- Class with the `abstract` keyword.
- Contains at least one abstract method.
- Cannot be instantiated (objects cannot be created).
- May contain non-abstract methods.
- Can have static and non-static variables.
  
🔵 **Abstract Class vs Interface**

**Abstract Class:**

- Can have both abstract and non-abstract methods.
- Provides partial implementation of abstraction.
- Can have constructors.
- Can have static and non-static variables.
- Can implement interfaces.

**Interface:**

- Contains only abstract methods.
- Provides 100% implementation of abstraction.
- Cannot have constructors.
- Can only have static and final variables.
- Cannot implement abstract classes.
- Java 8 allows defining default and static methods in interfaces.

🔵 **Keywords in Different Cases of Inheritance**
- `interface` to `interface`: `extends`   
- `interface` to `class`: `implements`     
- `Class` to `Class`: `extends`    
- `Class` to `Interface`: Not possible    
- `Abstract Class` to `Class`: `extends`    

**Note:**   
- A class can extend another class and implement interfaces simultaneously.    
- When implementing multiple interfaces, extend the class before implementing the interfaces.     

## 3. Marker Interface 

<table>
    <tr>
        <td><a href="#">
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">3. Marker Interface</th>
    </tr>
</table>

🔵 **Marker interface**    
Marker interface is an interface that has no methods or fields. It is used to mark a class as having some property or behavior.
     
## 4. Encapsulation

<table>
    <tr>
        <td><a href="#">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">4. Encapsulation</th>
    </tr>
</table>

Encapsulation is the process of wrapping code and data together into a single unit. It provides control over data by restricting direct access to some of its components, allowing only setter or getter methods.

## 5. Type Casting

<table>
    <tr>
        <td><a href="#">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">5. Type Casting</th>
    </tr>
</table>

🔵 **Implicit And Explicit Type Casting**

Type casting refers to assigning one data type to another type. Java supports widening and narrowing casting, as well as auto boxing and unboxing through wrapper classes.

🔵 **Wrapper Classes**

Wrapper classes are datatype supported classes, use to represent values in form of objects, when we convert primitive data types into objects (boxing) and objects back to primitive data types (unboxing).

🔵 **Boxing, Unboxing And AutoBoxing**    
**Usecase 1:**  
`int x = 10;`   
`Integer integer = new Integer(x); //Boxing`  
**Usecase 2:**  
`Integer integer = 10; //AutoBoxing`     
`Integer integer = x; //AutoBoxing`  
**Usecase 3:**  
`Integer integer = new Integer(10);`     
`int x=integer; //unboxing`  
**Usecase 4:**  
`if(x<integer) { //unboxing }`

🔵 **Upcasting and Downcasting**

- **Upcasting**: Storing a child object in a parent type reference variable.
- **Downcasting**: Storing a parent object in a child type reference variable, which requires explicit casting.

**Usecase 1:**  
`Parent parent = new Child(); //upcasting`     
`Parent parent = new Child();`      
`parent.setAge(10);`      
`Child child = (Child) parent; //downcasting`

**Usecase 2:**  
`Parent parent = new Parent();`      
`Child child = (Child) parent; // class cast exception`

**Usecase 3:**  
`Abc abc = new Xyz(); // doesn’t have any relation then class cast exception`

## 6. Object class

<table>
    <tr>
        <td><a href="#">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">6. Object Class and Equality vs equals method</th>
    </tr>
</table>

  - Tostring
  - Equals
  - Hashcode
  - Clone
  - Tostring
  - getClass
  - Wait
  - Notify
  - Notifyall
  - Finalize

🔵**Equality vs equals method**

## 7.ToString method
<table>
    <tr>
        <td><a href="#">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">7.ToString method</th>
    </tr>
</table>    

```java
class Abc{
int property=10 ;

public static void main(String[] a){
Abc abc = new Abc();
Sysout(abc.toString());
}
}

Abc abc = new Abc(); //1000 →   2000  → reference id

Abc@hashcode
```


