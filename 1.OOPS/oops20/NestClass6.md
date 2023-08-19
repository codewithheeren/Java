## OOPS - Nested Class

### NestClass6.java

```java
/**
 *  Data shadowing in inner class
 * @author Heeren
 * @version 1.0
 */
package com.java.oops20;

class Outer5 {
	int x = 10;

	class Inner {
		private int x = 20;

		void display() {
			int x = 30;
			System.out.println(x);
			System.out.println(this.x);
			System.out.println(Outer5.this.x);
		}
	}
}

public class NestClass6 {
	public static void main(String args[]) {
		Outer5 outer = new Outer5();
		Outer5.Inner inner = outer.new Inner();
		inner.display();
	}
}
```
---