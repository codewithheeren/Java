### Break singleton pattern using Cloneable

```java

/**
 *   
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.singleton;

class SuperClass implements Cloneable {

	String variable = "property";

	@Override
	protected Object clone() throws CloneNotSupportedException {
		return super.clone();
	}
}

class Singleton extends SuperClass {
	public static Singleton instance = new Singleton();

	private Singleton() {
	}
}

public class SingletonAccess {
	public static void main(String[] args) throws CloneNotSupportedException {
		Singleton instance1 = Singleton.instance;
		Singleton instance2 = (Singleton) instance1.clone();
		System.out.println("instance1 hashCode:- " + instance1.hashCode());
		System.out.println("instance2 hashCode:- " + instance2.hashCode());
	}
}

```
---

### Overcome Cloning issue as following 

```java
/**
 *   
 * @author Heeren
 * @version 1.0
 */
 
package com.codewithheeren.singleton;

class SuperClass implements Cloneable {
	String variable = "property";

	@Override
	protected Object clone() throws CloneNotSupportedException {
		return super.clone();
	}
}

class Singleton extends SuperClass {
	public static Singleton instance = new Singleton();

	private Singleton() {
	}

	@Override
	protected Object clone() throws CloneNotSupportedException {
		return instance;
	}
}

public class SingletonAccess {

	public static void main(String[] args) throws CloneNotSupportedException {
		Singleton instance1 = Singleton.instance;
		Singleton instance2 = (Singleton) instance1.clone();
		System.out.println("instance1 hashCode:- " + instance1.hashCode());
		System.out.println("instance2 hashCode:- " + instance2.hashCode());
	}
}
```
---