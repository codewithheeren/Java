## Static Method

### StaticMethod1.java

```java
/**
 * Static Method implementation - 
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.java8;

@FunctionalInterface
interface MathOperation {
    int operate(int a, int b);

    static int add(int a, int b) {
        return a + b;
    }

    static int subtract(int a, int b) {
        return a - b;
    }
}

public class StaticMethod1 {
    public static void main(String[] args) {
        int x = 10;
        int y = 5;

        int result1 = MathOperation.add(x, y);
        int result2 = MathOperation.subtract(x, y);

        System.out.println("Addition: " + result1);
        System.out.println("Subtraction: " + result2);
    }
}

```
---
