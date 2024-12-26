## OOPS - Nested Class

### NestClass2.java

```java
/**
 * Instance data memeber of outer class is not allowed in static inner class
 * @author Heeren
 * @version 1.0
 */
package com.java.oops20;

class Outer1 {
	static int x = 10;
	int y = 20;

	static class StaticInner {
		static void show() {
			System.out.println(x);
//			System.out.println(y); // that is not allowed
		}

	}
}

public class NestClass2 {
	public static void main(String args[]) {
		Outer1.StaticInner.show();
		Outer1.StaticInner inner = new Outer1.StaticInner();
		inner.show();
	}
}
```
---