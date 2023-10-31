## Functional Interface - Supplier

### SupplierExample.java

```java
/**
 * Supplier implementation - 
 * Supplier does not take any input, produces a result when called, and returns a value. 
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.java8;

import java.util.Random;
import java.util.function.Supplier;

public class SupplierExample {
    public static void main(String[] args) {
        Supplier<Integer> randomNumberSupplier = () -> {
            Random random = new Random();
            return random.nextInt(100);
        };

        int randomValue = randomNumberSupplier.get();
        System.out.println("Random Number: " + randomValue);
    }
}

```
---
