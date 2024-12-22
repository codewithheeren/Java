## OOPS - Static block

### MathUtils.java

```java
/**
 * Static block implementation
 * @author Heeren
 * @version 1.0
 */
package com.java.oops13;

public class MathUtils {
	private static double pi;

	static {
		// Static initialization block
		pi = 3.14159;
		System.out.println("Static block initializing Pi value");
	}

	public static double getPi() {
		return pi;
	}

	public static void main(String[] args) {
		System.out.println("Value of Pi: " + MathUtils.getPi());
	}
}

```
---
