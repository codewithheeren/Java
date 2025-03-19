## Reflection

```java
/** 
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.reflection;

public class Person {
	public String personName;
	private String nationality;
	protected String BloodGroup;

	public Person() {
		super();
	}

	public Person(String personName) {
		super();
		this.personName = personName;
	}

	public void setPersonName(String personName) {
		this.personName = personName;
	}

	public void setNationality(String nationality) {
		this.nationality = nationality;
	}

	public void setBloodGroup(String bloodGroup) {
		BloodGroup = bloodGroup;
	}

	private void privateInformation() {
		System.out.println("private information can not accessible outside the class.");
	}

	public String getInfo() {
		return "Person [personName=" + personName + ", nationality=" + nationality + ", BloodGroup=" + BloodGroup + "]";
	}

}

```
---

```java
/**
 * Fatching methods metadata of Person class using reflection  
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.reflection;

import java.lang.reflect.Method;
import java.lang.reflect.Modifier;

public class ReflectionImpl1 {

	public static void main(String[] args) {
		Person person = new Person();
		Class obj = person.getClass();
		Method[] methods = obj.getDeclaredMethods();
		for (Method m : methods) {
			System.out.println("Method Name: " + m.getName());
			int modifier = m.getModifiers();
			System.out.println("Modifier: " + Modifier.toString(modifier));
			System.out.println("Return Types: " + m.getReturnType());
			System.out.println("=======================================");
		}
	}
}
```
---