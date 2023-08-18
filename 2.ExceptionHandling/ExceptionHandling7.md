## Exception Handling - Finally block

### ExceptionHandling7.java

```java
/**
 * finally block implementation.
 * finally executes regardless of exception occurred or not  
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.exception;

public class ExceptionHandling7 {
	public static void main(String args[]) {
		try {
			int data = 25 / 5;
			System.out.println(data);
		} catch (NullPointerException e) {
			System.out.println(e);
		}
		finally {
			System.out.println("finally block is always executed");
		}
		System.out.println("rest of code...");
	}
}
```
---