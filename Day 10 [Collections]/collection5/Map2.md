## Collection - Map Implementation

### Map2.java

```java
/**
 * Looping of Map implementations
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.collection5;

import java.util.HashMap;
import java.util.Iterator;
import java.util.Map;
import java.util.Set;

public class Map2 {
	public static void main(String[] args) {

		Map<Integer, String> map = new HashMap<>();
		map.put(5, "Eban");
		map.put(2, "Timmy");
		map.put(9, "Jimmy");
		map.put(6, "John");
		map.put(1, "Vikky");
		map.put(12, "Tom");
		System.out.println(map);

		Set<Integer> set = map.keySet();
		for (Integer key : set) {
			System.out.println("key- " + key + " value-" + map.get(key));
		}

		System.out.println("-------------------------------------------------------");
		Iterator<Map.Entry<Integer, String>> itr = map.entrySet().iterator();
		while (itr.hasNext()) {
			Map.Entry<Integer, String> entry = itr.next();
			System.out.println("key- " + entry.getKey() + " value-" + entry.getValue());
		}

		System.out.println("-------------------------------------------------------");
		for (String name : map.values()) {
			System.out.println(name);
		}
	}
}
```
---
