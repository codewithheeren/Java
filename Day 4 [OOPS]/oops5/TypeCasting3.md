## OOPS - TypeCasting 

### TypeCasting3.java

```java
/**
 * Explicit Typecasting
 * @author Heeren
 * @version 1.0
 */
package com.java.oops18;

public class TypeCasting3 {
	public static void main(String[] args) {
		double doubleValue = 123.45;
		int intValue = (int) doubleValue; // Explicit type casting
		System.out.println("Double value: " + doubleValue);
		System.out.println("Int value: " + intValue);

		char charValue = 'A';
		int unicode = (int) charValue; // Explicit type casting
		System.out.println("Char value: " + charValue);
		System.out.println("Unicode value: " + unicode);
	}
}
```
---