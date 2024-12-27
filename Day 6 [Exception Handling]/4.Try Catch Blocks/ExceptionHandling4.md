## Exception Handling - Unreachable code

### ExceptionHandling4.java

```java
/**
 * Example of Unreachable code.
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.exception;

import java.util.Scanner;

public class ExceptionHandling4 {

	public static void main(String[] args) {
		try {
			int a[] = new int[5];
			a[5] = 30 / 0;
		} /*catch (Exception e) {
			System.out.println("Parent Exception occurs");
		}*/ catch (ArithmeticException e) {
			System.out.println("Arithmetic Exception occurs");
		}
		catch (ArrayIndexOutOfBoundsException e) {
			System.out.println("ArrayIndexOutOfBounds Exception occurs");
		}
		System.out.println("rest of the code");
	}
}
```
---