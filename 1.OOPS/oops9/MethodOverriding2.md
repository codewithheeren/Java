## OOPS - Method Overriding

### MethodOverriding2.java

```java
/**
 * Implementation of calling of super class method using super keyword.(method overriding) 
 * @author Heeren
 * @version 1.0
 */
package com.java.oops9;

class Base1 {
	public void method() {
		System.out.println("Base Class : method()");
	}
}

class Child1 extends Base1 {
	public void method() {
		System.out.println("Child Class : method()");
	}

	public void accessParentMethod() {
		super.method();
	}
}

public class MethodOverriding2 {
	public static void main(String[] args) {
		Child1 child = new Child1();
		child.method();
		child.accessParentMethod();
	}
}
```
---