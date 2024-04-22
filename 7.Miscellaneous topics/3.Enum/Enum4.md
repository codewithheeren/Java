## Enum

```java
/**
 * Nested Enum
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.enum;
class EnumImpl {
	enum Season{   
		WINTER, SPRING, SUMMER, FALL;   
	}

	public static void main(String args[]) {
		for (Season s : Season.values())
			System.out.println(s+" ordinal value is "+s.ordinal());

	}
}
```
---
