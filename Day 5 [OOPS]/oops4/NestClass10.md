## OOPS - Nested Class

### NestClass10.java

```java
/**
 * Local inner class can not change the value of the method's variable in which it is defined.
 * @author Heeren
 * @version 1.0
 */
package com.java.oops20;

class Outer10 {
	public void method() {
		int localVariable = 100;
		class LocalInner {
			void display() {
//				localVariable = 200;
				System.out.println(localVariable);
				System.out.println("local inner class");
			}
		}
		LocalInner inner = new LocalInner();
		inner.display();

	}
}

public class NestClass10 {
	public static void main(String args[]) {
		Outer10 outer = new Outer10();
		outer.method();
	}
}
```
---