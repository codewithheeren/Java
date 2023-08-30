## Collection - Map Implementation

### Map1.java

```java
/**
 * Map methods implementations
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.collection5;

import java.util.Collection;
import java.util.HashMap;
import java.util.Map;
import java.util.Set;

public class Map1 {
	public static void main(String[] args) {

		Map<Integer, String> map = new HashMap<>();
		map.put(5, "Eban");
		map.put(2, "Timmy");
		map.put(9, "Jimmy");
		map.put(6, "John");
		map.put(1, "Vikky");
		map.put(12, "Tom");
		System.out.println(map);

		System.out.println("------------------Access all values of map");
		Collection<String> names = map.values();
		System.out.println(names);

		System.out.println("------------------Access all keys of map");
		Set<Integer> keys = map.keySet();
		System.out.println(keys);

//		String name = map.get(9);
//		System.out.println(name);
//		
//		map.put(5,"Heeren");
//		System.out.println(map);
	}
}
```
---
