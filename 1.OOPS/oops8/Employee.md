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
	public static void main(String[] args) {
	Department department = new Department();
	department.setDepartmentName("Production Department");
	System.out.println(department.DepartmentName);
	}
}
```
---