/**
 * Implementation of static and instance data members
 * @author Heeren
 * @version 1.0
 */
package com.java.oops6;
// method overlaoding by chaning no of para. and data types of para.
public class Employee {
	
	private String ename;
	private int salary; 
	
	public void changeData(String ename,int salary)
	{
		this.ename=ename;
		this.salary=salary;
	}
	
	public void changeData(String ename)
	{
		this.ename = ename;
	}

	public void changeData(int salary)
	{
		this.salary= salary;
	}
	
	public void displayData() {
		System.out.println(ename);
		System.out.println(salary);
	}
	
	public static void main(String[] args) {
		Employee employee = new Employee();
		employee.changeData(55000);
		employee.displayData();
	}
}

