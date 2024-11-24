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
	private int id;
	private String name;
	private double price;
	private static int count = 0;

	{
		count++;
		id = count;
	}

	public Product() {

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

	public int getId() {
		return id;
	}

	public static int getCount() {
		return count;
	}

	public static void main(String[] args) {
		Product p1 = new Product("laptop", 900);
		Product p2 = new Product("mobile");
		Product p3 = new Product();

		System.out.println("Total objects created: " + Product.getCount());
		System.out.println(p1.getName() + " id: " + p1.getId());
		System.out.println(p2.getName() + " id: " + p2.getId());
		System.out.println(p3.getName() + " id: " + p3.getId());
	}
}

```
---
