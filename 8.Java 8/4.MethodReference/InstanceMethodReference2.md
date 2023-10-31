## Instance Method Reference 

### InstanceMethodReference1.java

```java
/**
 * Predefine Instance Method Reference implementation - 
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.java8;

import java.util.Arrays;
import java.util.List;

public class InstanceMethodReference2 {
    public static void main(String[] args) {
        List<String> fruits = Arrays.asList("apple", "banana", "cherry", "date");

        String target = "cherry";

        fruits.stream()
				.filter(target::equals)
               .forEach(fruit -> System.out.println("Found: " + fruit));
    }
}

```
---
