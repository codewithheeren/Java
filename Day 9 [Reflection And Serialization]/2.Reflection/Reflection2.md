## Reflection

```java
/** 
 * Fatching Person's class variables informations 
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.reflection;

import java.lang.reflect.Field;
import java.lang.reflect.Method;
import java.lang.reflect.Modifier;

public class ReflectionImpl2 {

	public static void main(String[] args)
			throws IllegalArgumentException, IllegalAccessException, NoSuchFieldException, SecurityException {
		Person person = new Person();
		Class obj = person.getClass();

		Field field1 = obj.getField("personName");
		field1.set(person, "Tom");

		String value = (String) field1.get(person);
		System.out.println("Value: " + value);

		int mod = field1.getModifiers();
		String modifier1 = Modifier.toString(mod);
		System.out.println("Modifier: " + modifier1);
		System.out.println(person.getInfo());
	}
}

```
---
