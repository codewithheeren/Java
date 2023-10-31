## Functional Interface - Consumer

### ConsumerExample.java

```java
/**
 * Consumer implementation - 
 * Consumer takes an input, performs some action on it, and does not return any value.
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.java8;

import java.util.Arrays;
import java.util.List;
import java.util.function.Consumer;

public class ConsumerExample {
	public static void main(String[] args) {
		List<String> names = Arrays.asList("Alice", "Bob", "Charlie", "David");
		Consumer<String> namePrinter = (name) -> {
			System.out.println("Hello, " + name);
		};

		names.forEach(namePrinter);
	}
}

```
---
