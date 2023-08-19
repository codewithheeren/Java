## OOPS - Constructor

### Person2.java

```java
/**
 * Constructor Implementation : Default constructor
 * default constructor only creates when no costuructor 
 * available in the class.
 * @author Heeren
 * @version 1.0
 */
package com.java.oops11;

public class Person2 {
	private String name;
	private int age;

	public Person2(String name, int age) {
		this.name = name;
		this.age = age;
	}
	
	public Person2() {}

	public void printDetails() {
		System.out.println("Name : " + name);
		System.out.println("Age : " + age);
	}

	public static void main(String[] args) {
		Person2 person1 = new Person2("Timmy", 30);
		Person2 person2 = new Person2();
		person1.printDetails();
		person2.printDetails();
	}
}
```
---