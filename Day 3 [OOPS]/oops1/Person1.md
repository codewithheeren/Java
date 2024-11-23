## OOPS - Constructor 

### Person1.java

```java
/**
 * Constructor Implementation : Parameterize constructor
 * Initializing class level properties
 * @author Heeren
 * @version 1.0
 */
package com.java.oops11;

public class Person1 {
	private String name;
	private int age;

	public Person1(String name, int age) {
		this.name = name;
		this.age = age;
	}

	public String getName() {
		return name;
	}

	public int getAge() {
		return age;
	}

	public static void main(String[] args) {
		Person1 person1 = new Person1("Timmy", 30);
		Person1 person2 = new Person1("John", 25);
		
		System.out.println(person1.getName());
		System.out.println(person2.getAge());
	}
}
```
---