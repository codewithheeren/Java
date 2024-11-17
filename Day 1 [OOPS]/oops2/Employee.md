## OOPS - static and instance data members

### Employee.java

```java
/**
 * Implementation of static and instance data members
 * @author Heeren
 * @version 1.0
 */
package com.java.oops2;
public class Employee {
	static String cname;
	String ename;
	int esalary;

	public static void main(String[] args) {

	Employee.cname="HCL";
	System.out.println("company name is "+Employee.cname);
	Employee employee1 = new Employee();
	Employee employee2 = new Employee();
	employee1.ename="Tom";
	employee2.esalary=50000;
	System.out.println("Employee1 name : "+employee1.ename);
	System.out.println("Employee1 salary : "+employee1.esalary);
	System.out.println("Employee2 name : "+employee2.ename);
	System.out.println("Employee2 salary : "+employee2.esalary);
	}
}
```
---