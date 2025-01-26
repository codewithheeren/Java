## OOPS - Nested Class

### NestClass12.java

```java
/**
 * 2 step process of using interface without Anonymous inner class  
 * @author Heeren
 * @version 1.0
 */
package com.java.oops20;

interface Base {
	void method();
}

class Child implements Base {
	@Override
	public void method() {
		System.out.println("Implementation Class: method()");
	}
}

public class NestClass12 {
	public static void main(String[] s) {
		Base base = new Child();
		base.method();
	}
}
```
---