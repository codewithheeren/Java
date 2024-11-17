## OOPS - Data Hiding 

### MainClass.java

```java
/**
 * This class implements data hiding.
 * @author Heeren
 * @version 1.0
 */
package com.java.oops10;

class Base{
	int x = 10;
}

class Child extends Base {
	int x = 20;
	void method() {
		int x = 30;
		System.out.println("Local variable : "+x);
		System.out.println("class level variable : "+ this.x); // data shadowing
		System.out.println("base class variable : "+ super.x); // data hiding 
	}
}

public class MainClass {
	public static void main(String[] args) {
		Child child = new Child();
		child.method();
	}
}
```
---