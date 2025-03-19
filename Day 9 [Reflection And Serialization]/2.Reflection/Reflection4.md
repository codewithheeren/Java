## Reflection

```java
/** 
 * fatching all constructor informations
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.reflection;

import java.lang.reflect.Constructor;
import java.lang.reflect.Field;
import java.lang.reflect.Method;
import java.lang.reflect.Modifier;

public class ReflectionImpl4 {

	public static void main(String[] args)
			throws IllegalArgumentException, IllegalAccessException, NoSuchFieldException, SecurityException {
		Person person = new Person();
		Class obj = person.getClass();
		Constructor[] constructors = obj.getDeclaredConstructors();

		for (Constructor c : constructors) {
			System.out.println("Constructor Name: " + c.getName());
			int modifier = c.getModifiers();
			String mod = Modifier.toString(modifier);
			System.out.println("Modifier: " + mod);
			System.out.println("Parameters: " + c.getParameterCount());
			System.out.println("");
		}
	}
}

```
---
