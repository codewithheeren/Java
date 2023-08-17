## OOPS - Instance Variable

### JavaClass2.java

```java
/**
 * This class implements Instance Variable.
 * @author Heeren
 * @version 1.0
 */
package com.java.oops1;
public class JavaClass2 {
//	instance properties are different for each object.
    int x;
	public static void main(String[] args) {
		JavaClass2 object1 = new JavaClass2();
		JavaClass2 object2 = new JavaClass2();
		JavaClass2 object3 = new JavaClass2();
		object1.x = 10;
		object2.x = 20;
		object3.x = 30;
		System.out.println("Object1 x = "+object1.x);
		System.out.println("Object2 x = "+object2.x);
		System.out.println("Object3 x = "+object3.x);
	}
}
```
---