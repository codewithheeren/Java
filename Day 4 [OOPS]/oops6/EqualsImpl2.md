## OOPS - Equals method behavious in wrapper classes 

### ObjectImpl2.java

```java
/**
 * Object Class : equals method behavious in string class
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.java.oops6;

public class ObjectImpl2 {
	public static void main(String[] args) {
		String s1 = new String("Hello");
		String s2 = new String("Hello");
		if(s1==s2) 
			System.out.println("true"); 
		else 
			System.out.println("false"); 

		if (s1.equals(s2))
			System.out.println("true");
		else
			System.out.println("false");
	}
}
```
---
