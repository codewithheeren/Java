## Collection - List useful methods

### CustomArrayList1.java

```java
/**
 * useful methods implementation of list collection
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.collection1;

import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;

public class CustomArrayList3 {
	public static void main(String[] args) {
		List<String> list = new ArrayList<>();
		list.add("Hello");
		list.add("Hi");
		list.add("bye");
		list.add("How are you");
		list.add("See you.");
		System.out.println("checking of existance of any element in list - "+list.contains("Hello"));
		System.out.println(list);
		
		list.remove("bye");
		System.out.println(list);
		
		List<String> list2 = new ArrayList<>();
		list2.add("Tom");
		list2.add("John");
		list2.add("Timmy");
		
		list.addAll(list2); //add collection in existing colleciton.
		System.out.println(list);
		
		//converting list to array.
		String[] array = new String[list.size()];
		list.toArray(array);
		System.out.println("printing array - \n");
		for(String value : array) {
			System.out.print(value+",");
		}
		
		
		System.out.println("\nprinting array without using loop - "+Arrays.toString(array));
	}
}
```
---
