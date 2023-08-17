## OOPS - Method Overriding

### MethodOverriding3.java

```java
/**
 * Implementation of method overriding by changing access modifiers.
 * @version 1.0
 */
package com.java.oops9;

//Default -> protected -> public 
class Base2 {
	protected void method() {
		System.out.println("Base Class : method()");
	}
}

class Child2 extends Base1 {
	public void method() {
		System.out.println("Child Class : method()");
	}
}

public class MethodOverriding3 {
	public static void main(String[] args) {
		Child2 child = new Child2();
		child.method();
	}
}
```
---