## Java 8 features

 @author Heeren

 **Topics Covered**
--------------
    
--------------

**Q.what are the features of java 8**?

1.Lambda Expression

2.Functional Interface

3.Default Method

**4.Predicates**

**5.Functions**

6.Stream api

7.**Date time api**

8.Static methods

-   Lambda expression
    -   A way to define anonymous method
    -   Define A method without any name
    -   It provides a clear and concise way to represent one method interface using an expression
    -   helps to iterate, filter and extract data from collection.
    -   Ex1: more than 1 statement
**(int a, int b)->{**

**Sysout(“lambda expression”);**

                                                         **}**

-   Ex2: only 1 statement
**(int a) -> sysout(“single statement”);**

-   Ex 3: don’t need to declare parameter type
                               **(a,b) -> sysout(“single statement”);**

-   Ex 4: one parameter
                                   **a-> sysout(“single statement”);**

-   ex 5:
**a -> return a\*A;**

-   ex 6: don’t need to put return keyword in order to return
    -   **a -> (a\*a);** or **a -> a+a;**
-   Functional Interface
    -   Any interface having only one abstract method is functional interface
    -   Example of Functional Interface
        -   Runnable, Callable, Comparable
    -   To define functional interface, you need to have annotation @FunctionalInterface above the interface
    -   Ex 1:
        -   @FunctionalInterface
        -   interface CustomInterface {
            -   void method();
        -   }
    -   Ex 2 // invalid case, more than 1 method
        -   @FunctionalInterface
        -   interface CustomInterface {
            -   void method1();
            -   voidmethod2(); // invalid
        -   }
    -   Ex 2 // no method also invalid
        -   @FunctionalInterface
        -   interface CustomInterface {
        -   }
    -   Ex 3 // no method but inherit 1 method from parent interface // valid
        -   @FunctionalInterface
        -   interface OtherInterface {

void method();

-   }
-
-   @FunctionalInterface
-   interface CustomInterface extends OtherInterface{
-   } // valid
-   Ex 4 // valid same method in both parent and child // valid
    -   @FunctionalInterface
    -   interface OtherInterface {
    -   void method();
    -   }
    -
    -   @FunctionalInterface
    -   interface CustomInterface extends OtherInterface{
        -   void method(); // valid
    -   }
-   Ex 5 // can have default method or static method // valid
    -   @FunctionalInterface
    -   interface CustomInterface {
    -   void method();
    -   // default method or static method // valid
    -   }

Differences between anonymous class vs lambda expression

-   Cannot compare, one is class and another is a method
-   Lambda work with functional interface

Consumer and supplier

Consumer takes an input, performs some action on it, and does not return any value. It is used for operations that consume data or perform side effects.

Supplier does not take any input, produces a result when called, and returns a value. It is used for operations that provide or supply data.

-   Default methods for interface in Java 8
    -   Use default keyword to define them
    -   Interfaces can have default methods with implementation in Java 8 on later.
    -   Interfaces can have static methods as well, similar to static methods in classes.
    -   Default methods were introduced to provide backward compatibility for old interfaces so that they can have new methods without affecting existing code.
    -   Default method name should not match with any method name of object class
-   Static methods for interface in Java 8
    -   From java 8 we can define static method in interface
    -   It is a static method which belongs to the interface only. We can write implementation of this method in interface itself
    -   Static method can invoke only on interface class not on class.
    -   Interface and implementing class, both can have static method with the same name without overriding each other.
    -   Can only use it by using Interface name
    -   Interface static method will not by default available to its implementation class
    -   Can define self-executable interface by defining static main method inside interface
-   Predicates
    -   It is a functional interface which represents a predicate (boolean-valued function) of one argument.
    -   It is defined in the java.util.function package and contains test() a functional method.
    -   Boolean check that you can write in one line
    -   Syntax
        -   Interface Predicates<T>{
            -   Boolean test(T t);
        -   }
    -   Ex:
        -   int x = 15;
        -   Predicate<Integer> predicate = x -> x>18;
        -   If (predicate.test(20)){ sysout(“……..”)
    -   And(), or(), negate()
-   Function
    -   Java.util.function.\*;
    -   to implement functional programming in Java. It represents a function which takes in one argument and produces a result
    -   interface Function<T,R>{
        -   R apply(T t);
    -   }
    -   Ex:
        -   String s = “Hello”;
        -   Function<String, Integer> function = x -> x.length();
        -   Sysout(function.apply(s));
-   Function
    -   Java.util.function.\*;
    -   to implement functional programming in Java. It represents a function which takes in one argument and produces a result
    -   interface Function<T,R>{
    -   R apply(T t);
    -   }
    -   Ex:
    -   String s = “Hello”;
    -   Function<String, Integer> function = x -> x.length();
    -   Sysout(function.apply(s));
-   Method reference
    -   used to refer method of functional interface.
    -   It is compact and easy form of lambda expression.
    -   Each time when you are using lambda expression to just referring a method, you can replace your lambda expression with method reference.
    -   Type of method references:
        -   Reference to a static method.
            -   Aregument type of the method reference should be the same as argument type in functional interface
        -   Reference to an instance method.
        -   Reference to a constructor.
**Method Reference**

-   Static method reference
-   Instance method reference
-   Constructor reference
**Optional -**

Avoiding Null References: Optional encourages you to wrap values that might be null in an Optional object, making it clear that a value could be absent.

Null-Safe Operations: You can use methods like ifPresent, orElse, orElseGet, and orElseThrow to safely work with the contained value or provide default values or exception handling when the value is absent.

Functional Approach: Optional supports functional programming by allowing you to chain methods to process the value when it's present. This makes code more concise and readable.

---
