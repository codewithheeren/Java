## OOPS - Local variable and Data shadowing

### CustomClass.java

```java
/**
 * Implementation of local variable and Data shadowing
 * @author Heeren
 * @version 1.0
 */
package com.java.oops5;
class CustomClass {
	int x = 10;

	public void display() {
		int x = 20;
		System.out.println(x);
		System.out.println(this.x);
	}

	public static void main(String[] a) {
		CustomClass customClass = new CustomClass();
		customClass.display();
	}
}
```
---