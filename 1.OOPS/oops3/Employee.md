/**
 * Implementation of static and instance data members
 * @author Heeren
 * @version 1.0
 */
package com.java.oops3;
//Static method implementation 
public class Employee {
	static String cname;
	String ename;
	int esalary;

	static void changeCname(String cn)
	{
		cname = cn;
	}

	public static void main(String[] args) {

	Employee.cname="HCL";
	System.out.println("Company Name : "+Employee.cname);
	
	System.out.println("Access directly Company Name : "+cname);
	
	Employee employee1 = new Employee();
	employee1.changeCname("TCS");
	Employee employee2 = new Employee();
	
	System.out.println("employee1 comapany name : "+employee1.cname);
	System.out.println("employee2 comapany name : "+employee2.cname);
	}
}


