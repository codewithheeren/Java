## OOPS - Nested Class

### NestClass4.java

```java
/**
 * Instance nested class can access static and instance both type of class memebers of outer class.
 * @author Heeren
 * @version 1.0
 */
package com.java.oops20;

class Outer3 {
	static int x = 10;
	int y = 20;

	class Inner {
		void show() {
			System.out.println(x);
			System.out.println(y);
		}
	}
}

public class NestClass4 {
	public static void main(String args[]) {
		Outer3 outer = new Outer3();
		Outer3.Inner inner = outer.new Inner();
		inner.show();
	}
}
```
---