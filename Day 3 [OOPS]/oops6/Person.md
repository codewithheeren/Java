## OOPS - final keyword

### Person.java

```java
/**
 * final key word  : blank final static and 
 * instance data memebers
 * final class can�t inherit, 
 * final method can�t override,
 * final variable cannot be change
 * @author Heeren
 * @version 1.0
 */
package com.java.oops14;

public class Person {
	final String NAME;
	final static String CNAME;

	static {
		CNAME = "HCL";
	}
	
    public Person(String name) {
        this.NAME = name;
    }

	public void displayData() {
		System.out.println("Person Name: " + NAME);
		System.out.println("Company Name: " + CNAME);
	}

	public static void main(String[] args) {
		Person person = new Person("John");
		person.displayData();
	}
}
```
---
