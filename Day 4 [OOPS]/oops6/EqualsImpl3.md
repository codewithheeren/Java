## OOPS - Object Class Implementations 

### ObjectImpl3.java

```java
/**
 * Object Class : Override equals method
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.java.oops6;

class Student {

	private String name;
	private int rollNo;

	public Student(String name, int rollNo) {
		super();
		this.name = name;
		this.rollNo = rollNo;
	}

	public boolean equals(Student obj) {
		if (rollNo != obj.rollNo)
			return false;
		return true;
	}
}

public class ObjectImpl3 {
	public static void main(String[] args) {
		Student demo1 = new Student("John", 21);
		Student demo2 = new Student("Tom", 33);
		Student demo3 = new Student("John", 21);

		if (demo1.equals(demo3))
			System.out.println(true);
		else
			System.out.println(false);
	}
}
```
---