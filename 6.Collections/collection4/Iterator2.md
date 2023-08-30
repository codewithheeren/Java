## Collection - List Iterator
### Iterator2.java

```java
/**
 * ListIterator implementation
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.collection4;

import java.util.ArrayList;
import java.util.List;
import java.util.ListIterator;

public class Iterator2 {
	public static List<Integer> method(List<Integer> list) {
		ListIterator<Integer> itr = list.listIterator();
		int i = 0;
		while (itr.hasPrevious()) {
			Integer x = (Integer) itr.previous();
			if (x % 2 != 0)
				itr.remove();
			if (x == 8)
				itr.set(100);
			if (x == 4)
				itr.add(200);
			else {

//				int y = list.get(i);
//				itr.set(y+1);
			}

			i++;
		}
		return list;
	}

	public static void main(String[] args) {
		List<Integer> list = new ArrayList<>();
		for (int i = 1; i <= 10; i++) {
			list.add(i);
		}
		System.out.println(method(list));
	}

}
```
---
