## Function Interface 

### Function1.java

```java
/**
 * Function Inteface implementation - 
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.java8;

import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
import java.util.function.Function;

public class Function1 {
	public static void main(String[] args) {
		List<Integer> numbers = new ArrayList<>(Arrays.asList(2, 4, 6, 8, 10));
		Function<Integer, Integer> square = num -> num * num;
		List<Integer> squares = new ArrayList<>();
		for (Integer number : numbers) {
			squares.add(square.apply(number));
		}
		System.out.println(squares);
	}
}

```
---
