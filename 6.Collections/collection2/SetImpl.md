## Collection - Custom sorting using comparator

### SetImpl.java

```java
/**
 * Default sorting and custom sorting implementation 
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.collection2;

import java.util.LinkedHashSet;
import java.util.Set;
import java.util.TreeSet;

public class SetImpl {
	public static void main(String[] args) {
		Set<Integer> linkedHashset = new LinkedHashSet<>();
		linkedHashset.add(5);
		linkedHashset.add(1);
		linkedHashset.add(9);
		linkedHashset.add(2);
		linkedHashset.add(4);
		linkedHashset.add(3);
		System.out.println("linkedHashset-\n" + linkedHashset);

		Set<Integer> set = new TreeSet<>();
		set.add(5);
		set.add(1);
		set.add(9);
		set.add(2);
		set.add(4);
		set.add(3);
		System.out.println("TreeSet- \n" + set);
		
		Set<Integer> customSet = new TreeSet<>(new CustomCompartor());
		customSet.add(5);
		customSet.add(1);
		customSet.add(9);
		customSet.add(2);
		customSet.add(4);
		customSet.add(3);
		System.out.println("Custom Sorted set - \n" + customSet);
	}

}
```
---