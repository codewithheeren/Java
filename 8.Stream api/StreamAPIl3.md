## Stream API Implementation

### StreamAPIl2.java

```java
/**
 * Intermediate operations in stream api
 * intermediate methods
 * max
 * min
 * @author Heeren
 * @version 1.0
 */
package com.logical.streamLevel1;

import java.util.stream.Collectors;
import java.util.stream.Stream;

public class StreamAPIl3 {
	public static void main(String[] args) {
		// 1
		// removing vovels from string
		String string1 = "Hello";
		Stream<Character> charstream = string1.chars().mapToObj(s -> (char) s);
		// charstream.filter(c->(c != 'e')&&(c != 'o')).forEach(System.out::println);

		// 2
		// converting intger values into one string
		String s2 = Stream.of(1, 2, 3, 4, 5).map(String::valueOf).collect(Collectors.joining());
		// System.out.println(s2);

		// 3
		// count no of elements
		long count = Stream.of(1, 2, 6, 7).count();
		// System.out.println(count);

		// 4
		// retrieve only first two even numbers.
		// Stream.of(1,3,2,12,6,7).filter(i->i%2==0).limit(2).forEach(System.out::println);

		// 5
		// remove duplicate elements from collection
		Integer[] arrayunique = Stream.of(1, 2, 3, 4, 5, 3, 1, 6, 2, 7).distinct().toArray(Integer[]::new);
		// System.out.println(Arrays.toString(arrayunique));
	}
}
```
---
