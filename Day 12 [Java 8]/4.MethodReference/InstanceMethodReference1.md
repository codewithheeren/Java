## Instance Method Reference 

### InstanceMethodReference1.java

```java
/**
 * Custom Instance Method Reference implementation - 
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.java8;

@FunctionalInterface
interface MyStringConcatenator {
	String concatenate(String str1, String str2);
}

public class InstanceMethodReference1 {
	public static void main(String[] args) {
		InstanceMethodReference1 methodReference = new InstanceMethodReference1();
		MyStringConcatenator concatenator = methodReference::customConcatenate;

		String result = concatenator.concatenate("Hello, ", "World!");
		System.out.println("Concatenated String: " + result);
	}

	public String customConcatenate(String str1, String str2) {
		return str1 + str2;
	}
}

```
---
