## Collection - List Implementation

### CustomArrayList1.java

```java
/**
 * Allow heterogeneous elements 
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.collection1;

import java.util.ArrayList;
import java.util.List;

public class CustomArrayList1 {
	public static void main(String[] args) {
		List list = new ArrayList();
		list.add("Hello");
		list.add(1);
		list.add(2.345);
		list.add(true);
		System.out.println(list);
	}
}
```
---
