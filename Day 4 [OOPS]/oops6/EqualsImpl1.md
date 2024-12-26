## OOPS - Default Equals method implementation

### OObjectImpl1.java

```java
/**
 * Object Class : Default equals method implementation
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.java.oops6;

public class ObjectImpl1 {
	public static void main(String[] args) {
		ObjectImpl1 object1 = new ObjectImpl1();
		ObjectImpl1 object2 = new ObjectImpl1();
		if(object1==object2) 
			System.out.println("true"); 
		else 
			System.out.println("false"); 

		if (object1.equals(object2))
			System.out.println("true");
		else
			System.out.println("false");
	}
}
```
---