## Reflection

```java
/** 
 * fatching all variables informations
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.reflection;

import java.lang.reflect.Field;
import java.lang.reflect.Method;
import java.lang.reflect.Modifier;


public class ReflectionImpl3 {

	public static void main(String[] args)
			throws IllegalArgumentException, IllegalAccessException, NoSuchFieldException, SecurityException {
		Person person = new Person();
		Class obj = person.getClass();

		Field[] fields = obj.getDeclaredFields();
		for (Field field : fields) {
			System.out.println("field Name: " + field.getName());
			int modifier = field.getModifiers();
			System.out.println("Modifier: " + Modifier.toString(modifier));
			System.out.println("Data Types: " + field.getType());
			System.out.println(" ");
		}
		;
	}
}

```
---
