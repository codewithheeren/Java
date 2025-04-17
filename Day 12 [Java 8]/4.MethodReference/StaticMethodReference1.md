## Static Method Reference 

### StaticMethodReference1.java

```java
/**
 * Custom Static Method Reference implementation - 
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.java8;

@FunctionalInterface
interface MySquareFunction {
	int square(int n);
}

public class StaticMethodReference1 {
	public static void main(String[] args) {
		MySquareFunction squareFunction = StaticMethodReference1::calculateSquare;

		int result = squareFunction.square(5);
		System.out.println("Square: " + result);
	}

	public static int calculateSquare(int n) {
		return n * n;
	}
}

```
---
