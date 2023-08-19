## OOPS - Constructor chaining 

### Employee1.java

```java
/**
 * Constructor chaining within class implementation  
 * Initializing class level properties
 * @author Heeren
 * @version 1.0
 */
package com.java.oops13;

public class Employee1 {
	private String ename;
	private float salary;
	private int age;

	public Employee1(String ename, float salary, int age) {
		this.ename = ename;
		this.salary = salary;
		this.age = age;
	}

	public Employee1(String ename, int age) {
		this(25000);
		this.ename = ename;
		this.age = age;
	}

	public Employee1(float salary) {
		this.salary = salary;
	}

	public void printData() {
		System.out.println("Employee name is - " + ename);
		System.out.println("Employee salary is - " + salary);
		System.out.println("Employee age is - " + age);
	}

	public static void main(String[] args) {
		Employee1 employee = new Employee1("Minh", 25);
		employee.printData();

	}

}

```
---