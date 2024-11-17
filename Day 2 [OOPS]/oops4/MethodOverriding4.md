## OOPS - Method Overriding

### MethodOverriding4.java

```java
/**
 * Implementation of method overriding by changing return type (covariant type) 
 * @author Heeren
 * @version 1.0
 */
package com.java.oops9;

class A {
}

class B extends A {
}

class Base3 {
	A method() {
		System.out.println("Base Class : method()");
		return new A();
	}
}

class Child3 extends Base3 {
	B method() {
		System.out.println("Child Class : method()");
		return new B();
	}
}

public class MethodOverriding4 {
	public static void main(String[] args) {
		Child3 child = new Child3();
		child.method();
	}
}
```
---