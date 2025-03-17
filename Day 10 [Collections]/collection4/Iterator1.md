## Collection - Iterator

### Iterator1.java

```java
/**
 * Removing even even numbers from a list. 
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.collection4;

import java.util.ArrayList;
import java.util.Iterator;
import java.util.List;

public class Iterator1 {
	public static List<Integer> method(List<Integer> list) {
		Iterator<Integer> itr = list.iterator();
		while (itr.hasNext()) {
			Integer x = (Integer) itr.next();
			if (x % 2 == 0)
				itr.remove();
		}
		return list;
	}

	public static void main(String[] args) {
		List<Integer> list  = new ArrayList<>();
		for(int i= 1;i<=10;i++) {
			list.add(i);
		}
		System.out.println(method(list));
	}

}
```
---
