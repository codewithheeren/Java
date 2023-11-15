### Break singleton pattern using Reflection 

```java
/**
 *  
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.singleton;

import java.lang.reflect.Constructor;

class Singleton {
	public static Singleton instance = new Singleton();

	private Singleton() {
	}
}

public class SingletonAccess {

	public static void main(String[] args) {
		Singleton instance1 = Singleton.instance;
		Singleton instance2 = null;
		try {
			Constructor[] constructors = Singleton.class.getDeclaredConstructors();
			for (Constructor constructor : constructors) {
				constructor.setAccessible(true);
				instance2 = (Singleton) constructor.newInstance();
				break;
			}
		} catch (Exception e) {
			e.printStackTrace();
		}

		System.out.println("instance1.hashCode():- " + instance1.hashCode());
		System.out.println("instance2.hashCode():- " + instance2.hashCode());
	}
}
```
---

### Overcome reflection issue as following 

```java
package com.codewithheeren.singleton;

public enum Singleton {
    INSTANCE;
}

```
---