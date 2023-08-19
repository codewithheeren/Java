## OOPS - Init block 

### Product.java

```java
/**
 * Init block implementation
 * Initializing class level properties
 * @author Heeren
 * @version 1.0
 */
package com.java.oops12;

public class Product {
	private String name;
	private double price;

	{
		price = 10.0; // Initialize price to a minimum value
		System.out.println(this); // This holds current object reference
		System.out.println("Price initialized to minimum value: " + price);
	}

	public Product(String name, double price) {
		this.name = name;
		this.price = price;
	}

	public Product(String name) {
		this.name = name;
	}

	public String getName() {
		return name;
	}

	public double getPrice() {
		return price;
	}

	public static void main(String[] args) {
		Product product1 = new Product("Grocery Item", 25.0);
		Product product2 = new Product("Gadget");

		System.out.println(product1.getName() + " Price: " + product1.getPrice());
		System.out.println(product2.getName() + " Price: " + product2.getPrice());
	}
}

```
---