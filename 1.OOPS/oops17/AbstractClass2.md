## OOPS - Abstract Class 

### AbstractClass2.java

```java
/**
 * Abstract Class : Why constructor is allow to define inside abstract class
 * @author Heeren
 * @version 1.0
 */

package com.java.oops17;

abstract class Base {
	int x, y;

	Base(int x, int y) {
		this.x = x;
		this.y = y;
	}

	abstract void printProperties();

	void display() {
		System.out.println("display functionality");
	}
}

class Child extends Base {

	int a;

	Child(int a, int x, int y) {
		super(x, y);
		this.a = a;
	}

	void printProperties() {
		System.out.println(a);
		System.out.println(x);
		System.out.println(y);
	}
}

public class AbstractClass2 {
	public static void main(String args[]) {
		Child child = new Child(10, 20, 30);
		child.printProperties();
	}
}
```
---