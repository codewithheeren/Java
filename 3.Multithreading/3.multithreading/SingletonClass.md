## Singleton class implementation.

### Approach 1

```java
/**
 * 
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.singleton;
class Singleton {

   private static Singleton instance = new Singleton();
   private Singleton(){}
   public static Singleton getInstance(){
      return instance;
   }
}

public class MainClass {

	public static void main(String[] args) {
		Singleton singleton = Singleton.getInstance();
		System.out.println(singleton);
	}
}

```
---

### Approach 2

```java
/**
 * 
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.singleton;
public class Singleton {

	private static Singleton instance;
	static {
		instance = new Singleton();
	}

	private Singleton() {
	}

	public static Singleton getInstance() {
		return instance;
	}
}


```
---

### Approach 3

```java
/**
 * 
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.singleton;
public class Singleton {

	private static Singleton instance;

	private Singleton() {
	}

	public static synchronized Singleton getInstance() {
		if (instance == null) {
			instance = new Singleton();
		}
		return instance;
	}
}


```
---

### Approach 4

```java
/**
 * 
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.singleton;
public class Singleton {

	private static Singleton instance;

	private Singleton() {
	}

	public static Singleton getInstance() {
		if (instance == null) {
			synchronized (Singleton.class) {
				if (instance == null) {
					instance = new Singleton();
				}
			}
		}
		return instance;
	}
}

```
---
### Approach 5

```java
/**
 * 
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.singleton;
public class BillPughSingleton {
    private BillPughSingleton() {
        // Private constructor to prevent instantiation from other classes.
    }

    private static class SingletonHelper {
        private static final BillPughSingleton INSTANCE = new BillPughSingleton();
    }

    public static BillPughSingleton getInstance() {
        return SingletonHelper.INSTANCE;
    }
}

```
---