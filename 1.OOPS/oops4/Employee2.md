## OOPS - Instance Method 

### Employee.java

```java
/**
 * Instance method implementation 
 * @author Heeren
 * @version 1.0
 */
package com.java.oops4;
public class Employee2 {
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
    
	void displayResult() {
		System.out.println("Companay name - "+cname);
		System.out.println("employee details - \n name- "+ename+"\nsalary- "+esalary);
		System.out.println("------------------------------");
	}
	public static void main(String[] args) {
	
	Employee2.changeCname("Epam Systems");
	Employee2 employee1 = new Employee2();
	employee1.change("Tim", 50000);
	Employee2 employee2 = new Employee2();
	employee2.change("Jimmy", 90000);
	
	employee1.displayResult();
	employee2.displayResult();
	}
}
```
---

