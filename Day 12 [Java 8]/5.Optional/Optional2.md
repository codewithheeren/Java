## Optional Implementation

### Optional2.java

```java
/**
 * Demonstrates Chaining Operations with optional object
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.java8;
import java.util.Optional;

public class Optional2 {
	public static void main(String[] args) {
		Optional<String> maybeName = Optional.ofNullable(getName());
		String result = maybeName.map(String::toUpperCase).orElse("No name provided");
		System.out.println("Result: " + result);
	}

	public static String getName() {
		// Simulate a method that might return null
		return "Alice";
	}
}

```
---
