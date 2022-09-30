## Cloning

### Student.java

```java
/**
 * This class implements simple cloning.
 * @author Heeren
 * @version 1.0
 */
public class Student implements Cloneable {
	int rollno;
	String name;

	Student(int rollno, String name) {
		this.rollno = rollno;
		this.name = name;
	}

	public Object clone() throws CloneNotSupportedException {
		return super.clone();
	}

	public static void main(String args[]) {
		try {
			Student s1 = new Student(101, "John");
			Student s2 = (Student) s1.clone();
			System.out.println(s1.rollno + " " + s1.name);
			System.out.println(s2.rollno + " " + s2.name);

		} catch (CloneNotSupportedException c) {
		}

	}
}
```
---

### Student.java  
```java
/**
 * This class implements Primitive injection  using setters.
 * @author heeren
 * @version 1.0
 */
p

	
```
---

### MainClass.java
```java

```
---