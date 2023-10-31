## Function Interface 

### Function2.java

```java
/**
 * Function Inteface implementation - 
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.java8;

import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
import java.util.function.Function;

public class Function2 {
    public static void main(String[] args) {
        List<String> names = new ArrayList<>(Arrays.asList("Alice", "Bob", "Charlie", "David"));
        Function<String, String> toUppercase = str -> str.toUpperCase();

        List<String> uppercaseNames = new ArrayList<>();
        for (String name : names) {
            uppercaseNames.add(toUppercase.apply(name));
        }

       System.out.println(uppercaseNames);
    }
}

```
---
