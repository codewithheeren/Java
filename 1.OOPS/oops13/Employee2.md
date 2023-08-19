## OOPS - Constructor chaining 

### Employee2.java

```java
/**
 * Constructor chaining out side the class implementation  
 * this or super must be the first statement of constructor
 * @author Heeren
 * @version 1.0
 */
package com.java.oops13;

class Company {
	String cname;

	Company(String cname) {
		this.cname = cname;
	}
	
	public Company() {
		super();
	}
}

public class Employee2 extends Company {
	private String ename;
	private float salary;
	private int age;

	public Employee2(String ename, float salary, int age) {
		this.ename = ename;
		this.salary = salary;
		this.age = age;
	}

	public Employee2(String ename, int age) {
		this(25000);
		this.ename = ename;
		this.age = age;
	}

	public Employee2(float salary) {
		super("HCL");
		this.salary = salary;
	}

	public void printData() {
		System.out.println("Employee name is - " + ename);
		System.out.println("Employee salary is - " + salary);
		System.out.println("Employee age is - " + age);
		System.out.println("Employee company name is - " + cname);
	}

	public static void main(String[] args) {
		Employee2 employee = new Employee2("5Minh", 2);
		employee.printData();

	}

}

```
---