## OOPS - Custom Immutable class implementation

### Main1.java

```java

/**
 * Emmutable class implementation.
 * Rules to Create immutable class -
 * Class must be final 
 * Class data members must be private and final .
 * Do not define any setter method in that class.
 * Data members must initialize using constructor only. 
 * @author Heeren
 * @version 1.0
 */
package com.java.oops21;

public class Main1 {
	public static void main(String[] args) {
		Person person = new Person("John", "D.", 30);

		System.out.println("First Name: " + person.getFirstName());
		System.out.println("Last Name: " + person.getLastName());
		System.out.println("Age: " + person.getAge());

		// Attempting to modify the person object (which is not possible)
//		 person.setAge(31); // This will not compile

		System.out.println(person);
	}
}

```
---
