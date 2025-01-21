## OOPS Day 4

**Topics Covered**
--------------
1. [Abstraction And Interfaces](#1-abstraction-and-interfaces)
2. [Abstract Class And Difference b/w Abstract Class and Interface](#2-abstract-class-and-difference-bw-abstract-class-and-interface)
3. [Marker Interface](#3-marker-interface)
4. [Encapsulation](#4-encapsulation)
5. [Type Casting](#5-type-casting)
6. [Object Class and Equality vs equals method](#6-object-class-and-equality-vs-equals-method)
7. [ToString method](#7-tostring-method)
8. [Assignment](#8-assignment)
--------------
  
## 1. Abstraction And Interfaces

<table>
    <tr>
        <td><a href="https://youtu.be/Tm_esItAZ08">
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
            <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e4" alt="yt" width="20" height="20">
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
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e4" alt="yt" width="20" height="20">
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
`parent.setAge(10);`      
`Child child = (Child) parent; //downcasting`

**Usecase 2:**  
`Parent parent = new Parent();`      
`Child child = (Child) parent; // class cast exception`

**Usecase 3:**  
`Abc abc = new Xyz(); // doesn’t have any relation then class cast exception`

## 6. Object Class and Equality vs equals method

<table>
    <tr>
        <td><a href="#">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e4" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">6.1 Object Class</th>
    </tr>
</table>

  - Tostring
  - Equals
  - Hashcode
  - Clone
  - getClass
  - Wait
  - Notify
  - Notifyall
  - Finalize

<table>
    <tr>
        <td><a href="#">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e4" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">6.2 Equality vs equals method</th>
    </tr>
</table>

In Java, Use == for reference comparison and equals() for value comparison.

## 7. ToString method
<table>
    <tr>
        <td><a href="#">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e4" alt="yt" width="20" height="20">
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
---
## 8. Assignment

**Task 1: Employee Management System with Abstract Classes and Interfaces**     
**Description:** Design an Employee Management System that utilizes abstract classes and interfaces for real-time features like salary calculation and role-based behavior.

1. **Abstract Class:**
   - Create an abstract class `Employee` with properties like `name`, `ID`, and methods like `calculateSalary()`.
   - Add an abstract method `performDuties()` for role-specific behavior.

2. **Interface:**
   - Implement an interface `Benefits` with methods like `getBonus()` and `getInsuranceDetails()`.

3. **Implementation:**
   - Create concrete classes `Manager`, `Developer`, and `Intern` that extend `Employee` and implement `Benefits`.

4. **Encapsulation:**
   - Use private properties with appropriate getter and setter methods.

5. **Real-Time Requirement:**
   - Each role should have different salary calculation logic and unique duties.
   - Provide an option to display benefits for employees based on their roles.

**Task 2: Banking System with Marker Interface**     
**Description:** Develop a banking system with a marker interface for VIP customer identification.

1. **Encapsulation:**
   - Create a `BankAccount` class with encapsulated properties like `accountNumber`, `balance`, and `holderName`.

2. **Marker Interface:**
   - Define a marker interface `VIPCustomer`.
   - Add a method `isVIP()` to check if the customer implements `VIPCustomer`.

3. **Implementation:**
   - Create classes `RegularCustomer` and `PremiumCustomer` extending `BankAccount`.
   - Use the marker interface for `PremiumCustomer` and provide additional privileges for VIPs (e.g., higher withdrawal limits).

4. **Real-Time Requirement:**
   - Implement functionality where VIP customers get exclusive benefits like personalized account management.

**Task 3: E-Commerce System with Encapsulation and Type Casting**    
**Description:** Build an E-Commerce system where products are stored in a collection, and runtime type casting is used to process different product types.

1. **Encapsulation:**
   - Create a `Product` class with properties like `productName`, `price`, and `category`.
   - Use encapsulated getters and setters.

2. **Type Casting:**
   - Create subclasses `Electronics`, `Clothing`, and `Books`.
   - Store all product types in a `List<Product>` and use type casting to access subclass-specific methods like `getWarranty()` for electronics.

3. **Real-Time Requirement:**
   - Add a method to calculate the discount for each product based on its category using type-specific logic.

**Task 4: Equality vs. `equals()` in Real-Time Systems**    
**Description:** Implement a real-time contact management application to demonstrate the difference between `==` and `equals()`.

1. **Object Class:**
   - Create a `Contact` class with properties like `name`, `phoneNumber`, and `email`.

2. **Overriding `equals()` and `hashCode()`:**
   - Override `equals()` to compare `Contact` objects based on `phoneNumber`.
   - Override `hashCode()` to maintain consistency.

3. **Real-Time Requirement:**
   - Store `Contact` objects in a `HashSet` and demonstrate how overriding `equals()` and `hashCode()` affects duplicate handling.

**Task 5: Custom `toString()` Implementation in a Library Management System**    
**Description:** Create a library management system with a meaningful `toString()` implementation for displaying book details.

1. **Object Class:**
   - Create a `Book` class with properties like `title`, `author`, `ISBN`, and `price`.

2. **Custom `toString()`:**
   - Override the `toString()` method to display book details in a readable format.

3. **Real-Time Requirement:**
   - Create a `Library` class to manage a collection of books and display their details using `toString()`.

**Task 6:**      
Create a double type variable for account balance. Explicitly cast it to int when displaying rounded-off values. Implement this in a BankAccount class with a displayBalance() method.   

**Task 7:**    
Create an ArrayList to store item prices using boxing. Retrieve the prices from the list, unbox them, and calculate the total cost in a ShoppingCart class.


