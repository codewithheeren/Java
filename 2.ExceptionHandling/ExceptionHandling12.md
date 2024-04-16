## Exception Handling 

### ExceptionHandling12.java

```java
/**
 * UseCase 1 parent method in throwing checked exception and child is not throwing any exception. 
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.exception;
import java.io.IOException;

class Superclass {
    public void readFile() throws IOException {
        System.out.println("Reading file in superclass");
        throw new IOException("IO Exception occurred");
    }
}

class Subclass extends Superclass {
    @Override
    public void readFile() {
        try {
            System.out.println("Reading file in subclass");
            super.readFile();
        } catch (IOException e) {
            System.out.println("Handled IOException in subclass: " + e.getMessage());
        }
    }
}

public class ExceptionHandling12 {
    public static void main(String[] args) {
        Superclass obj = new Subclass();
        try {
            obj.readFile();
        } catch (IOException e) {
            System.out.println("Caught IOException in main method: " + e.getMessage());
        }
    }
}

```
---
