## OOPS - final keyword

### Employee.java

```java
/**
 * anonymous object  
 * @author Heeren
 * @version 1.0
 */
package com.java.oops14;

public class Employee {
	private String ename;
	private float salary;
	private int age;

	public Employee() {
		System.out.println("Constructor Invoke.");
	}
	
	public Employee(String ename, float salary, int age) {
		this.ename = ename;
		this.salary = salary;
		this.age = age;
	}
	
	public void changeData(String ename, float salary, int age) {
		this.ename = ename;
		this.salary = salary;
		this.age = age;
	}

	public void printData() {
		System.out.println("Employee name is - " + ename);
		System.out.println("Employee salary is - " + salary);
		System.out.println("Employee age is - " + age);
	}

	public static void main(String[] args) {
		Employee employee = new Employee("Kim",2000,21);
		employee.printData();
		new Employee("John", 3000, 22).printData();

//		new Employee().changeData("John", 3000, 22);
//		new Employee().printData();
		
		// Need of holding reference
//		Employee employee = new Employee();
//		employee.changeData("Timmy", 20000, 18);
//		employee.printData();
	}

}
```
---