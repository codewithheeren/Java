## Static Method

### StaticMethod2.java

```java
/**
 * Static Method implementation - 
 * we use a static method from the java.util.stream.Stream interface. 
 * The "of" method creates a stream of strings.
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.java8;

import java.util.stream.Stream;

public class StaticMethod2 {
    public static void main(String[] args) {
        Stream<String> stream = Stream.of("Alice", "Bob", "Charlie", "David");

        long count = stream.filter(s -> s.length() > 4).count();
        System.out.println("Count of names with more than 4 characters: " + count);
    }
}


```
---
