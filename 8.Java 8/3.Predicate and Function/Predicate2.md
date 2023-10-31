## Predicate Method

### Predicate2.java

```java
/**
 * Predicate Method implementation - 
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.java8;

import java.util.Arrays;
import java.util.List;
import java.util.function.Predicate;

public class Predicate2 {
	public static void main(String[] args) {
		List<Integer> numbers = Arrays.asList(2, 4, 6, 7, 8, 10);

		Predicate<Integer> isEven = num -> num % 2 == 0;

		boolean allEven = numbers.stream().allMatch(isEven);

		if (allEven) {
			System.out.println("All numbers are even.");
		} else {
			System.out.println("Not all numbers are even.");
		}
	}
}

```
---
