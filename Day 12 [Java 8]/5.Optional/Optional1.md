## Optional Implementation

### Optional1.java

```java
/**
 * Demonstrates basic usage of Optional
 * If the optionalName contains a non-null value,
 * It's extracted using orElse
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.java8;

import java.util.Optional;

public class Optional1 {
	public static void main(String[] args) {
		Optional<String> optionalName = Optional.ofNullable(getName());
		String name = optionalName.orElse("Unknown");
		System.out.println("Name: " + name);
	}

	public static String getName() {
		// This method might return null
		return "John";
	}
}

```
---
