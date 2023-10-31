## Lambda Expression

### LambdaExpression1.java

```java
/**
 * Need of Lambda expression
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.java8;

@FunctionalInterface
interface CustomInterface {
	void welcome();
}

class InterfaceImpl implements CustomInterface {
	public void welcome() {
		System.out.println("Welcome to my project.");
	}
}

public class LambdaExpression1 {

	public static void main(String[] args) {
		CustomInterface object = new InterfaceImpl();
		object.welcome();
	}
}
```
---
```java
/**
 * Implementing Lambda expression
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.java8;

@FunctionalInterface
interface CustomInterface {
	void welcome();
}

public class LambdaExpression1 {
	public static void main(String[] args) {
		CustomInterface object = () -> System.out.println("Welcome to my project.");
		object.welcome();
	}
}
```
---