## Optional Implementation

### Optional3.java

```java
/**
 * Filter to check if the value inside optionalNumber is greater than 0.
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.java8;

import java.util.Optional;

public class Optional3 {
	public static void main(String[] args) {
		Optional<Integer> optionalNumber = Optional.ofNullable(getNumber());
		Optional<Integer> filtered = optionalNumber.filter(n -> n > 0);

		if (filtered.isPresent()) {
			System.out.println("Positive Number: " + filtered.get());
		} else {
			System.out.println("Not a positive number");
		}
	}

	public static Integer getNumber() {
		// Simulate a method that might return null
		return -5;
	}
}

```
---
