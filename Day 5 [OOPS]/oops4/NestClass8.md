## OOPS - Nested Class

### NestClass8.java

```java
/**
 * Local Inner class inside static method can only access static member of outer class.
 * @author Heeren
 * @version 1.0
 */
package com.java.oops20;

class Outer7 {
	int x = 10;
	static int y = 20;

	public static void method() { // static methods can only access static properties.
		class LocalInner {
			void display() {
				System.out.println(y);
				System.out.println("local inner class");
			}
		}
		LocalInner inner = new LocalInner();
		inner.display();
	}
}

public class NestClass8 {
	public static void main(String args[]) {
		Outer7 outer = new Outer7();
		outer.method();
	}
}
```
---