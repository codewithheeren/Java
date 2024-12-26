## OOPS - Nested Class

### NestClass7.java

```java
/**
 * Local Inner class
 * @author Heeren
 * @version 1.0
 */
package com.java.oops20;

class Outer6 {
	public void method() {
		class LocalInner {
			void display() {
				System.out.println("local inner class");
			}
		}
		LocalInner inner = new LocalInner();
		inner.display();
	}
}

public class NestClass7 {
	public static void main(String args[]) {
		Outer6 outer = new Outer6();
		outer.method();
	}
}
```
---