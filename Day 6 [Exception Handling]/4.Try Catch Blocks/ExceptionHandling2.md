## Exception Handling - Try-Catch block

### ExceptionHandling2.java

```java
/**
 * Implementation of Try Catch Handler.
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.exception;

import java.util.Scanner;

public class ExceptionHandling2 {
	public static void main(String args[]) {
		System.out.println("Enter first value");
		Scanner scanner = new Scanner(System.in);
		int x = scanner.nextInt();
		System.out.println("Enter second value");
		int y = scanner.nextInt();
		try {
			double data = x / y;
			System.out.println("Result : " + data);
		} catch (ArithmeticException e) {
			System.out.println(e);
		}
		System.out.println("rest of the code...");
	}
}
```
---