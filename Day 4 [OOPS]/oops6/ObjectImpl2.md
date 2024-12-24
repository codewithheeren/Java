## OOPS - Object Class Implementations 

### ObjectImpl2.java

```java
/**
 * Object Class : equals method implementation
 * @author Heeren
 * @version 1.0
 */
package com.java.oops19;

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

public class ObjectImpl2 {
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