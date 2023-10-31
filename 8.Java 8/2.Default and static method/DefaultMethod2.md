## Default Method

### DefaultMethod2.java

```java
/**
 * Default Method implementation - 
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.java8;

import java.util.ArrayList;
import java.util.List;

public class DefaultMethod2 {
	public static void main(String[] args) {
		List<String> names = new ArrayList<>();
		names.add("Alice");
		names.add("Bob");
		names.add("Charlie");
		names.add("David");

		// Using the forEach default method to print each name
		names.forEach(name -> System.out.println("Hello, " + name));
	}
}

```
---
