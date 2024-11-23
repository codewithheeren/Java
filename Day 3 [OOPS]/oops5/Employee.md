## OOPS - Call by reference

### Employee.java

```java
/**
 * Call by reference 
 * @author Heeren
 * @version 1.0
 */
package com.java.oops15;
class Employee {
	private String ename;
	private String age;
	private int salary;

	public void setEmployeeData(String ename, String age, int salary) {
		this.ename = ename;
		this.age = age;
		this.salary = salary;
	}

	public void setEmployeeData(Employee employee) {
		this.ename = employee.ename;
		this.age = employee.age;
		this.salary = employee.salary;
	}

	@Override
	public String toString() {
		return "Employee [ename=" + ename + ", age=" + age + ", salary=" + salary + "]";
	}

	public static void main(String[] args) {
		Employee employee1 = new Employee(); 
		employee1.setEmployeeData("Tom","25",2555);   // call by value
		System.out.println(employee1);
		Employee employee2 = new Employee();
		employee2.setEmployeeData(employee1);  //call by reference 
		System.out.println(employee2);
	}
}
```
---