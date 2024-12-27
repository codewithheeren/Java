## Exception Handling - Custom exception handling

### ExceptionHandling10.java

```java
/**
 * Custom exception handling
 * Custom exceptions are useful when you want to represent specific types
 * of errors that aren't available in predefine exception classes. 
 * That allow you to create a more meaningful and specialized error message in application.
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.exception;

class CustomException extends Exception {
    public CustomException(String message) {
        super(message);
    }
}

public class ExceptionHandling10 {
    public static void main(String[] args) {
        try {
            int num = 10;
            if (num > 5) {
                throw new CustomException("Number is greater than 5.");
            }
        } catch (CustomException e) {
              System.out.println(e);
//            System.out.println("Custom Exception Caught: " + e.getMessage());
        }
        System.out.println("Rest of the code...");
    }
}
```
---