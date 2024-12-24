## OOPS - Abstract Class 

### AbstractClass1.java

```java
/**
 * Abstract Class
 * @author Heeren
 * @version 1.0
 */
package com.java.oops17;

abstract class Shape {
	private String name;

	public Shape(String name) {
		this.name = name;
	}

	public String getName() {
		return name;
	}

	abstract double calculateArea();
}

class Circle extends Shape {
	private double radius;

	public Circle(String name, double radius) {
		super(name);
		this.radius = radius;
	}

	@Override
	double calculateArea() {
		return Math.PI * radius * radius;
	}
}

class Rectangle extends Shape {
	private double width;
	private double height;

	public Rectangle(String name, double width, double height) {
		super(name);
		this.width = width;
		this.height = height;
	}

	@Override
	double calculateArea() {
		return width * height;
	}
}

public class AbstractClass1 {
	public static void main(String[] args) {
		Circle circle = new Circle("Circle", 5.0);
		Rectangle rectangle = new Rectangle("Rectangle", 4.0, 6.0);

		System.out.println(circle.getName() + " Area: " + circle.calculateArea());
		System.out.println(rectangle.getName() + " Area: " + rectangle.calculateArea());
	}
}
```
---