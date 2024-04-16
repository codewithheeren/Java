## Exception propagation

### ExceptionHandling11.1.java

```java
/**
 * Exception propagation in case of unChecked Exceptions , those are automatically forward in calling chain.
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.exception;

public class ExceptionPropagation {

    public static void main(String[] args) {
        try {
            method1();
        } catch (Exception e) {
            System.out.println("Exception caught in main method: " + e);
        }
    }

    public static void method1() {
        System.out.println("Inside method1");
        method2();
    }

    public static void method2() {
        System.out.println("Inside method2");
        method3();
    }

    public static void method3() {
        System.out.println("Inside method3");
        // Simulate an exception
        int result = 10 / 0; // This line will throw an ArithmeticException
    }
}

```
---
**Exception propagation in case of Checked Exceptions , Those have to either handle or forcfully forward in calling chain using throws keyword.**
### ExceptionHandling11.2.java
```java
import java.io.IOException;

public class ExceptionPropagation {

    public static void main(String[] args) {
        try {
            method1();
        } catch (Exception e) {
            System.out.println("Exception caught in main method: " + e);
        }
    }

    public static void method1() throws IOException{
        System.out.println("Inside method1");
        method2();
    }

    public static void method2() throws IOException{
        System.out.println("Inside method2");
        method3();
    }

    public static void method3() throws IOException{
        System.out.println("Inside method3");
        throw new IOException();
    }
}
 
```
---
