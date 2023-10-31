## Default Method

### DefaultMethod1.java

```java
/**
 * Default Method implementation - 
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.java8;

interface Drawable {
	void draw(); // Abstract method

	default void drawDefault() {
		System.out.println("Default implementation: Drawing a shape.");
	}
}

class Circle implements Drawable {
	@Override
	public void draw() {
		System.out.println("Drawing a circle.");
	}
}

public class DefaultMethod1 {
	public static void main(String[] args) {
		Drawable circle = new Circle();
		circle.draw();
		circle.drawDefault();
	}
}


```
---
