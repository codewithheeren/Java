## Predicate Method

### Predicate1.java

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

public class Predicate1 {
	public static void main(String[] args) {
//eg. 1		
//		short a = 15;
//		Predicate<Integer> predicate = age -> {
//												if(age>18)
//													return true;
//												else
//													return false;
//										};
//		Predicate<Integer> predicate = age -> age>18;								
//		System.out.println(predicate.test((int) a));
//eg. 2		
		List<String> names = Arrays.asList("Alice", "Bob", "Charlie", "David", "Ella");
		Predicate<String> startsWithC = name -> name.startsWith("C");
		names.stream().filter(startsWithC).forEach(System.out::println);
	}
}

```
---
