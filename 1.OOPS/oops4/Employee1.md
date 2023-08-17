## OOPS - Instance method 

### Employee1.java

```java
/**
 * Implementation of Instance method 
 * @author Heeren
 * @version 1.0
 */
package com.java.oops4;
public class Employee1 {
	static String cname;
	String ename;
	int esalary;

	static void changeCname(String cn)
	{
		cname = cn;
	}
	
	void change(String en,int sal)
	{
	ename = en;
	esalary = sal;
	}

	public static void main(String[] args) {
	Employee1.cname="HCL";
	System.out.println("Company name : "+Employee1.cname);
	
	Employee1 emp1 = new Employee1();
	emp1.change("Tim", 50000);
	Employee1 emp2 = new Employee1();
	emp2.change("Jimmy", 90000);
	
	System.out.println("employee1 details - \n name- "+emp1.ename+"\nsalary- "+emp1.esalary);
	System.out.println("employee2 details - \n name- "+emp2.ename+"\nsalary- "+emp2.esalary);

	}
}
```
---