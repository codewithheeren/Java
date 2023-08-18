## Exception Handling - Try With Resource

### ExceptionHandling9.java

```java
/**
 * Try with resource implementation.
 * you don't need to explicitly close resources in a finally block,
 * the resources are automatically closed when the try block exits,
 * whether normally or due to an exception.
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.exception;

import java.io.BufferedReader;
import java.io.FileReader;
import java.io.IOException;

public class ExceptionHandling9 {
	public static void main(String[] args) {
		// The resource (BufferedReader) is declared inside the try-with-resources block.
		try (BufferedReader reader = new BufferedReader(new FileReader(".\\src\\resource\\testdata.txt"))) {
			String line;
			while ((line = reader.readLine()) != null) {
				System.out.println(line);
			}
		} catch (IOException e) {
			System.out.println("An error occurred while reading the file: " + e.getMessage());
		}
	}
}
```
---