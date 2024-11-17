## OOPS - Inheritance

### Employee.java

```java
/**
 * Implementation of Single inheritance
 * @author Heeren
 * @version 1.0
 */
package com.java.oops7;
class Department{
    String DepartmentName;
	public void setDepartmentName(String DepartmentName) {
		this.DepartmentName= DepartmentName;
	}
}

public class Employee extends Department{
	
	private String ename;
	private int salary; 
	
	public void changeData(String ename,int salary)
	{
		this.ename=ename;
		this.salary=salary;
	}
	
	public void displayData() {
		System.out.println("Department name is : "+DepartmentName);
		System.out.println("Employee name is : "+ename);
		System.out.println("Salary is : "+ salary);
	}
	
	public static void main(String[] args) {
		Employee employee = new Employee();
		employee.changeData("Evan",55000);
		employee.setDepartmentName("HR Dept");
		employee.displayData();
	}
}
```
---
