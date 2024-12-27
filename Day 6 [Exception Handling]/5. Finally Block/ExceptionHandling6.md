## Exception Handling - Finally block

### ExceptionHandling6.java

```java
/**
 * finally block implementation.
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.exception;

import java.io.BufferedReader;
import java.io.FileReader;
import java.io.IOException;

public class ExceptionHandling6 {
	public static void main(String[] args) {
		BufferedReader reader = null;
		try {
			reader = new BufferedReader(new FileReader(".\\src\\resource\\testdat.txt"));
			String line;
			while ((line = reader.readLine()) != null) {
				System.out.println(line);
			}
		} catch (IOException e) {
			System.out.println("An error occurred while reading the file: " + e.getMessage());
		} finally {
			// The finally block ensures that the file is closed
			// whether an exception occurred or not.
			if (reader != null) {
				try {
					reader.close();
				} catch (IOException e) {
					System.out.println("An error occurred while closing the file: " + e.getMessage());
				}
			}
		}
	}
}
```
---