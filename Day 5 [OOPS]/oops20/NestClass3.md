## OOPS - Nested Class

### NestClass3.java

```java
/**
 * static nested class can have static and instance both type of class memebers.
 * @author Heeren
 * @version 1.0
 */
package com.java.oops20;

class Outer2 {

	static class StaticInner {

		static void show() {
			System.out.println("static method: Inner class");
		}

		void display() {
			System.out.println("Instance method: Inner class");

		}
	}

	public static void main(String[] a) {

	}
}

public class NestClass3 {
	public static void main(String args[]) {
		Outer2.StaticInner.show();
		Outer2.StaticInner inner = new Outer2.StaticInner();
		inner.display();
	}
}
```
---