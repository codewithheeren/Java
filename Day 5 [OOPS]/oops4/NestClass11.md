## OOPS - Nested Class

### NestClass11.java

```java
/**
 * Anonymous inner class  
 * @author Heeren
 * @version 1.0
 */
package com.java.oops20;

interface Base {
	void method();
}

public class NestClass11 {
	public static void main(String[] s) {
		Base base = new Base() {
			public void method() {
				System.out.println("Implementation Class: method()");
			}
		};
		base.method();
	}
}
```
---