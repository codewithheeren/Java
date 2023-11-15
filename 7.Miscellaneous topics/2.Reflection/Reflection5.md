## Reflection

```java
/** 
 * Accessing private method
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.reflection;

import java.lang.reflect.Constructor;
import java.lang.reflect.Field;
import java.lang.reflect.InvocationTargetException;
import java.lang.reflect.Method;
import java.lang.reflect.Modifier;

public class ReflectionImpl5 {

	public static void main(String[] args) throws IllegalArgumentException, IllegalAccessException,
			NoSuchFieldException, SecurityException, NoSuchMethodException, InvocationTargetException {
		Person person = new Person();
		Class obj = person.getClass();
		Method method = obj.getDeclaredMethod("privateInformation");
		method.setAccessible(true);
		method.invoke(person);
	}
}

```
---
