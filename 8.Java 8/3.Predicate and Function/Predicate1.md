## Predicate Method

### Predicate1.java

```java
/**
 * Predicate Method implementation - 
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.java8;
package com.codewithheeren.java8;

import java.util.Arrays;
import java.util.List;
import java.util.function.Predicate;

public class Predicate1 {
	public static void main(String[] args) {
		List<String> names = Arrays.asList("Alice", "Bob", "Charlie", "David", "Ella");

		Predicate<String> startsWithC = name -> name.startsWith("C");

		names.stream().filter(startsWithC).forEach(System.out::println);
	}
}

```
---
