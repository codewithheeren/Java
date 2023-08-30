## Collection - Custom Comparator Implementation

### CustomComparator.java

```java
/**
 * Comparator implementation
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.collection3;

import java.util.Comparator;


public class CustomComparator implements Comparator<Employee>{

	@Override
	public int compare(Employee e1, Employee e2) {
		if(e1.getSalary()<e2.getSalary())
			return -1;
		if(e1.getSalary()>e2.getSalary())
			return 1;
		else
			return e1.getName().compareTo(e2.getName());
	}

}
```
---
