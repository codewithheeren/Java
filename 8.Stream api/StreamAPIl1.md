## Stream API Implementation

### StreamAPIl1.java

```java
/**
 * conversions to stream 
 * @author Heeren
 * @version 1.0
 */
package com.logical.streamLevel1;

import java.util.Arrays;
import java.util.stream.Stream;

public class StreamAPIl1 {
	public static void main(String[] args) {
		// 1
		Arrays.asList(2, 3, 1, 4, 5, 3).stream();

		// 2
		int[] array = { 1, 2, 3, 4, 5, 6 };
		Arrays.stream(array);

		// 3
		String string = "Hello";
		Stream<Character> stream = string.chars().mapToObj(s -> (char) s);
		// EG. - removing vovels from string
		// stream.filter(c->(c != 'e')&&(c != 'o')).forEach(System.out::println);

		// 4
		Stream.of(1, 2, 3, 4, 5, 6, 7).forEach(System.out::println);
	}
}
```
---
