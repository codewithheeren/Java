## OOPS - Association

### Employee.java

```java
/**
 * Implementation of Association
 * @author Heeren
 * @version 1.0
 */
package com.java.oops8;
class Department{
    String DepartmentName;
	public void setDepartmentName(String DepartmentName) {
		this.DepartmentName= DepartmentName;
	}
}

public class Employee {
	private String name;
	private int salary;
	public static void main(String[] args) {
		Department department = new Department();
		department.setDepartmentName("Production Department");
		Employee employee = new Employee();
		employee.name = "Heeren";
		employee.salary = 5000;
		System.out.println("Employee information: \nName:"+employee.name+"\nSalary:"+employee.salary+"\nDepartment:"+department.DepartmentName );
	}
}

```
---
