## Collection - Looping of collection

### CustomArrayList4.java

```java
/**
 * Looping of collection
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.collection1;

import java.util.ArrayList;
import java.util.Arrays;
import java.util.Iterator;
import java.util.List;
public class CustomArrayList4 {
	public static void main(String[] args) {
		List<String> list = new ArrayList<>();
		list.add("Hello");
		list.add("Hi");
		list.add("bye");
		list.add("How are you");
		list.add("See you.");

		// list itration
		// 1
		/*
		for (String value : list) {
			if (!(value.equals("Hi") || value.equals("See you.")))
				System.out.println(value);
		}
		*/
		
		/*
		Iterator<String> itr = list.iterator();
		while(itr.hasNext()) {
			String value = (String) itr.next();
			if(value.equals("Hi"))
				itr.remove();
		}
		System.out.println(list);
		*/
		
	}
}
```
---
