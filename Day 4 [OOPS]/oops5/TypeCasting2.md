## OOPS - TypeCasting 

### TypeCasting2.java

```java
/**
 * Boxing , AutoBoxing, UnBoxing
 * @author Heeren
 * @version 1.0
 */
package com.java.oops18;

public class TypeCasting2 {
	public static void main(String[] args) {
		int x = 10;

		// Boxing
		Integer integerBoxed = new Integer(x);
		System.out.println("Boxing, value- " + integerBoxed);

		// AutoBoxing
		Integer integerAutoBoxed1 = 10;
		Integer integerAutoBoxed2 = x;
		System.out.println("AutoBoxing, value- " + integerAutoBoxed2);

		// Unboxing
		Integer integerUnboxed = new Integer(10);
		int unboxedValue = integerUnboxed;
		System.out.println("UnBoxing, value- " + unboxedValue);

		// Unboxing while comparison
		if (x < integerUnboxed) {
			System.out.println("x is less than Unboxed value");
		} else {
			System.out.println("x is greater than or equal to Unboxed value");
		}
	}
}
```
---