## Java 8 features

 @author Heeren

 **Topics Covered**    
---
1.Lambda Expression   
2.Functional Interface  
3.Default Method   
4.Static methods   
5.Consumer and supplier
6.Predicates   
7.Functions   
8.Date time api   
9.Optional   
10.Stream api   

--- 

**Lambda expression**    
    -   A way to define anonymous method   
    -   It provides a clear and concise way to represent one method interface using an expression    
    -   helps to iterate, filter and extract data from collection.   
    -   Ex1: more than 1 statement   
    
**Lambda Expression possible definitions -**
```java

Ex1:	more than 1 statement
(int a, int b)->{ 
Sysout(“lambda expression”);
}

Ex2: only 1 statement
(int a) -> sysout(“single statement”);

Ex 3: don’t need to declare parameter type
(a,b) -> sysout(“single statement”);

Ex 4: one parameter without paranthesis
a-> sysout(“single statement”);

ex 5: 
a -> return a*A;

ex 6: don’t need to put return keyword to return value
a -> (a*a);		or 		a -> a*a;
```

-   Functional Interface
    -   Any interface having only one abstract method is functional interface
    -   Examples of Functional Interface
        -   Runnable, Callable, Comparable
    -   To define functional interface, you should annotate @FunctionalInterface above the interface
```java
Ex 1:
@FunctionalInterface
interface CustomInterface {
void method();
}
 
Ex 2:		// invalid case, more than 1 method
@FunctionalInterface
interface CustomInterface {
void method1();
void method2();		// invalid
}
 
Ex 3:	// no method also invalid
@FunctionalInterface
interface CustomInterface {
}

Ex 4:	// no method but inherit 1 method from parent interface	// valid
@FunctionalInterface
interface OtherInterface {
void method();
} 
@FunctionalInterface
interface CustomInterface extends OtherInterface{
} 				// valid

Ex 5:	// valid same method in both parent and child	// valid
@FunctionalInterface
interface OtherInterface {
void method();
} 
@FunctionalInterface
interface CustomInterface extends OtherInterface{
void method();				// valid
}

Ex 6:	// can have default method or static method 	// valid
@FunctionalInterface
interface CustomInterface {
void method();
// default method or static method		// valid
} 

```
**Differences between anonymous class vs lambda expression**

-   Cannot compare, one is class and another is a method
-   Lambda work with functional interface

**Default method**   
    -   Use default keyword to define them   
    -   Interfaces can have default methods with implementation in Java 8 on later.   
    -   Default methods were introduced to provide backward compatibility for old interfaces so that they can have new methods without affecting existing code.   
    -   Default method name should not match with any method name of object class   
         
**Static methods**   
    -   From java 8 we can define static method in interface   
    -   Static method can invoke only on interface not on class.   
    -   Interface static method will not by default available to its implementation class   
    -   Can define self-executable interface by defining static main method inside interface      
     
**Consumer and supplier**    
Consumer takes an input, performs some action on it, and does not return any value. It is used for operations that consume data or perform side effects.   
Supplier does not take any input, produces a result when called, and returns a value. It is used for operations that provide or supply data.    
   
**Predicates**
    -   It is a functional interface which represents a predicate (boolean-valued function) of one argument.   
    -   It is defined in the java.util.function package and contains test() a functional method.   
    -   Boolean check that you can write in one line   
 **Syntax and Example** 
 ```java
        Interface Predicates<T>{
          Boolean test(T t);
       }
  
        int x = 15;
        Predicate<Integer> predicate = x -> x>18;
        If (predicate.test(20)){
               sysout("....");
         }
         And(), or(), negate()
 ```   
**Function**
    - It represents a function which takes one argument and produces a result. 
  **Syntax and Example** 
  ```java
        interface Function<T,R>{
            R apply(T t);
        }
 
        String s = “Hello”;
        Function<String, Integer> function = x -> x.length();
        Sysout(function.apply(s));
```
  
**Method Reference**       
    -   used to refer method of functional interface.       
    -   It is compact and easy form of lambda expression.        
    -   Each time when you are using lambda expression to just referring a method, you can replace your lambda expression with method reference.         
    
    **Type of method references:**        
        -   Static method reference      
            -   Aregument type of the method reference should be the same as argument type in functional interface       
        -   Instance method reference       
        -   Constructor reference       

**Optional -**
- Optional is use to avoid Null References: Optional encourages you to wrap values that might be null in an Optional object, making it clear that a value could be absent.
- Null-Safe Operations: when the value is absent You can use methods like ifPresent, orElse, orElseGet, and orElseThrow to safely work with the contained value or provide default values or exception handling.
- Functional Approach: Optional supports functional programming by allowing you to chain methods to process the value when it's present. This makes code more concise and readable.

---
