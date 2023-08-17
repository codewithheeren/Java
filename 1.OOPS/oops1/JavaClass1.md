## OOPS - Static Variable 

### JavaClass1.java

```java
/**
 * This class implements Static Variable.
 * @author Heeren
 * @version 1.0
 */
 package com.java.oops1;
//static properties are common across multiple objects
public class JavaClass1 {
	static int x = 10;
	public static void main(String[] args) {
		JavaClass1 object1 = new JavaClass1();
		JavaClass1 object2 = new JavaClass1();
		JavaClass1 object3 = new JavaClass1();
		System.out.println("Object1 x = "+object1.x);
		System.out.println("Object2 x = "+object2.x);
		System.out.println("Object3 x = "+object3.x);
		
//		static property can also access using classname
		System.out.println("access by class name : "+JavaClass1.x);
		
		
	}
}
```
---
