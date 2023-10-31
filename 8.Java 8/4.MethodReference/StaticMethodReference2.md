## Static Method Reference 

### StaticMethodReference2.java

```java
/**
 * Predefine Static Method Reference implementation - 
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.java8;

import java.util.Arrays;
import java.util.List;

@FunctionalInterface
interface MySquareFunction {
	int square(int n);
}

public class StaticMethodReference2 {

	public static void main(String[] args) {
		List<String> numbers = Arrays.asList("1", "2", "3", "4", "5");
		numbers.stream().map(Integer::parseInt).forEach(System.out::println);
	}
}

```
---
