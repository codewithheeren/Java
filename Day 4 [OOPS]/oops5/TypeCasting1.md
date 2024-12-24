## OOPS - TypeCasting 

### TypeCasting1.java

```java
/**
 * Upcasting and downcasting
 * @author Heeren
 * @version 1.0
 */
package com.java.oops18;

class Parent {
	public void method() {
		System.out.println("method : Parent");
	}
}

class Child extends Parent {
	public void method() {
		System.out.println("method : Child");
	}
}

public class TypeCasting1 {
	public static void main(String args[]) {
		Child child = new Child();
		Parent parent = child; // upcasting
		parent.method();
		
		Child child1 = (Child) parent; // downcasting
		child1.method();

	}
}
```
---