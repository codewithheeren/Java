## Enum

```java
/**
 * Enum constructor implicitly called.
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.enum;
public enum Day {
	Sun, Mon, Tue, Wed, Thu, Fri, Sat;
	Day(){
		System.out.println("Invoke Constructor.");
	}
}
```
---
