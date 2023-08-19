## OOPS - Shallow cloning 

### ObjectImpl5.java

```java
/**
 * Shallow cloning 
 * @author Heeren
 * @version 1.0
 */
package com.java.oops19;

class School {
	String schoolName;
	String directorName;

	@Override
	public String toString() {
		return "School [schoolName=" + schoolName + ", directorName=" + directorName + "]";
	}

}

class Student2 implements Cloneable {
	String sName;
	int rollNo;
	School school;

	public Student2(String sName, int rollNo, School school) {
		super();
		this.sName = sName;
		this.rollNo = rollNo;
		this.school = school;
	}

	public Object clone() throws CloneNotSupportedException {
		return super.clone();
	}

	@Override
	public String toString() {
		return "Student [sName=" + sName + ", rollNo=" + rollNo + ", school=" + school + "]";
	}

}

public class ObjectImpl5 {
	public static void main(String[] args) throws CloneNotSupportedException {
		School school = new School(); // 1000
		school.schoolName = "DAV School"; // 1000
		Student2 student1 = new Student2("Tom", 45, school);
		Student2 student2 = (Student2) student1.clone();
		System.out.println(student1);
		System.out.println(student2);

		student1.school.schoolName = "DPS";
		System.out.println("-------------------------------------------------------------");
		System.out.println(student1);
		System.out.println(student2);

	}
}
```
---