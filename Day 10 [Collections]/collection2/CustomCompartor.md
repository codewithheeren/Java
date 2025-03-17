## Collection - Custom Compartor Implementation

### CustomCompartor.java

```java
/**
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.collection2;

import java.util.Comparator;

public class CustomCompartor implements Comparator<Integer>{

	@Override
	public int compare(Integer i1, Integer i2) {
		if(i1<i2)
			return 1;
		else if(i1>i2)
			return -1;
		else
			return 0;
	}

}
```
---