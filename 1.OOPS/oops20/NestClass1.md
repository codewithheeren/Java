## OOPS - Nested Class

### NestClass1.java

```java
/**
 * Static nested class
 * @author Heeren
 * @version 1.0
 */
package com.java.oops20;

class Outer {
	static int x = 10;
	static class StaticInner {
		static void show() {
			System.out.println("Static nested class : show()");
		}
	}
}

public class NestClass1 {
	public static void main(String args[]) {
		Outer.StaticInner.show();

		Outer.StaticInner inner = new Outer.StaticInner();
		inner.show();
	}
}
```
---
