## OOPS - Method Overriding

### MethodOverriding5.java

```java
/**
 * Implementation of method Hiding
 * @author Heeren
 * @version 1.0
 */
package com.java.oops9;

class Base4{
	static void method() {
	   System.out.println("Base Class : method()");
   }
}

class Child4 extends Base4{
	   static void method() {
		   System.out.println("Child Class : method()");
	   }
}

public class MethodOverriding5 {
	public static void main(String[] args) {
		Child4.method();
	}
}
```
---