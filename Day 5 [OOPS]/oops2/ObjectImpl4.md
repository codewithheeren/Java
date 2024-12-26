## OOPS - Object Class Implementations 

### ObjectImpl4.java

```java
/**
 * Object Class : clone method- cloning
 * @author Heeren
 * @version 1.0
 */
package com.java.oops19;

class Student1 implements Cloneable {
	int rollno;
	String name;

	Student1(int rollno, String name) {
		this.rollno = rollno;
		this.name = name;
	}

	public Object clone() throws CloneNotSupportedException {
		return super.clone();
	}
}
public class ObjectImpl4 {
	public static void main(String[] args) {
			try {
				Student1 s1 = new Student1(101, "John");
				Student1 s2 = (Student1) s1.clone();
				System.out.println(s1.rollno + " " + s1.name);
				System.out.println(s2.rollno + " " + s2.name);

			} catch (CloneNotSupportedException c) {
			}

	}
}
```
---