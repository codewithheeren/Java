## OOPS Day 4

 @author Heeren

 **Topics Covered**
--------------
 ### Mock Topics

- Abstraction
- Interface
- Abstract class
- Abstract class vs interface
- Marker Interface
- Encapsulation
- Type Casting
  - Upcasting and DownCasting
  - Boxing , UnBoxing and AutoBoxing
  - Implicit and Explicit Typecasting
-  Equality vs equals method 
- Object class
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

## Abstraction  

Abstraction is the process of showing functionality while hiding the implementation. It can be achieved in Java using interfaces or abstract classes.

### Interface      
![interface](https://github.com/codewithheeren/Java/assets/87074236/47c765b2-26ff-47c4-91d0-d7d267522525)   

- Blueprint of a class.

- Methods defined in interfaces are by default public and abstract.

- Interface data members are by default public, static, and final.

- Objects cannot be created from an interface.

- No constructor can be defined in an interface.

- When a class implements an interface, it needs to override all methods.

- Java supports multiple inheritance through interfaces (a class can implement multiple interfaces).

### Abstract Method

- Method without a body.

- Defined using the `abstract` keyword.

- Cannot be defined inside a concrete or normal class.

- Used in interfaces and abstract classes.

### Abstract Class

- Class with the `abstract` keyword.

- Contains at least one abstract method.

- Cannot be instantiated (objects cannot be created).

- May contain non-abstract methods.

- Can have static and non-static variables.

### Abstract Class vs Interface

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

### Keywords in Different Cases of Inheritance
---

- `interface` to `interface`: `extends`

- `interface` to `class`: `implements`

- `Class` to `Class`: `extends`

- `Class` to `Interface`: Not possible

- `Abstract Class` to `Class`: `extends`

**Notes:**

- A class can extend another class and implement interfaces simultaneously.

- When implementing multiple interfaces, extend the class before implementing the interfaces.

### Inner Interface

- Declaration of an inner interface occurs in the body of another interface or class.

- If declared in another class, it must be `static` but can have any access modifier.

- If declared in another interface, it must be `static` and `public`.

## Encapsulation

Encapsulation is the process of wrapping code and data together into a single unit. It provides control over data by restricting direct access to some of its components, allowing only setter or getter methods.

## Aggregation

Aggregation represents a weak association between classes where one class has an entity reference to another class. It is a "has-a" relationship and supports code reuse without maintaining an "is-a" relationship throughout the object's lifetime.

## Composition (HAS-A Relationship)

Composition is a strong association where one class is a part of another class. It represents a "part-of" relationship and involves creating objects of one class inside another class.

## Type Casting

Type casting refers to assigning one data type to another type. Java supports widening and narrowing casting, as well as auto boxing and unboxing through wrapper classes.

### Wrapper Classes

Wrapper classes are datatype supported classes, use to represent values in form of objects, when we convert primitive data types into objects (boxing) and objects back to primitive data types (unboxing).

**Usecase 1.**   
int x = 10;
Integer integer = new Integer(x); //Boxing    
**Usecase 2.**  
Integer integer = 10; //AutoBoxing
Integer integer = x;  //AutoBoxing   
**Usecase 3.**   
Integer integer = new Integer(10);
int x=integer; //unboxing    
**Usecase 4.**   
if(x<integer) {  //unboxing 

}

### Upcasting and Downcasting

- **Upcasting**: Storing a child object in a parent type reference variable.

- **Downcasting**: Storing a parent object in a child type reference variable, which requires explicit casting.   
**Usecase 1.**
Parent parent = new Child(); //upcasting
Parent parent = new Child();
parent.setAge(10);
Child child = (Child) parent; //downcasting   
**Usecase 2.**
Parent parent = new Parent();
Child child = (Child) parent; // class cast exception    
**Usecase 3.**
Abc abc = new Xyz(); // doesn’t have any relation then class cast exception


