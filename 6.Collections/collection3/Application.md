## Collection - Custom sorting

### Application.java

```java
/**
 * Arrange employee objects basis on the sorting order of their salary if the salary 
 * is same then arrange them in alphabetical order of their names.
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.collection3;

import java.util.Set;
import java.util.TreeSet;


public class Application {

	public static void main(String[] args) {
		Employee emp1 = new Employee(2,10000,"John");
		Employee emp2 = new Employee(8,2000,"Tom");
		Employee emp3 = new Employee(4,12000,"Tonny");
		Employee emp4 = new Employee(6,30000,"Andy");
		Employee emp5 = new Employee(1,30000,"zee");
		Set<Employee> set = new TreeSet<Employee>(new CustomComparator());
		set.add(emp1);                         
		set.add(emp2);
		set.add(emp3);
		set.add(emp4);
		set.add(emp5);
		System.out.println(set);	
	}
}

```
---





