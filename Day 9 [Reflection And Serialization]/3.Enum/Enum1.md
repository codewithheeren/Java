## Enum

```java
/**
 * Accessing enum value and converting enum value in to string.
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.enum;
public enum Color {
	black,white,yellow,orange;
}
```
---
```java
package com.codewithheeren.enum;
import java.util.Arrays;

public class Enum1 {
	public static void main(String[] args) {
		System.out.println(Color.black);
		Color color = Color.white;
		System.out.println(color);
		
		String colorConversion = color.toString();
		System.out.println(colorConversion);
	}
}
```
---
