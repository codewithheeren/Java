## OOPS - Deep cloning 

### ObjectImpl6.java

```java
/**
 * Deep cloning
 * @author Heeren
 * @version 1.0
 */
package com.java.oops19;

class School1 implements Cloneable {
	String schoolName;
	String directorName;

	public Object clone() throws CloneNotSupportedException {
		return super.clone();
	}

	@Override
	public String toString() {
		return "School [schoolName=" + schoolName + ", directorName=" + directorName + "]";
	}

}

class Student3 implements Cloneable {
	String sName;
	int rollNo;
	School1 school;

	public Student3(String sName, int rollNo, School1 school) {
		super();
		this.sName = sName;
		this.rollNo = rollNo;
		this.school = school;
	}

	public Object clone() throws CloneNotSupportedException {
		Student3 student = (Student3) super.clone();
		School1 school = (School1) this.school.clone();
		student.school = school;
		return student;
	}

	@Override
	public String toString() {
		return "Student [sName=" + sName + ", rollNo=" + rollNo + ", school=" + school + "]";
	}
}

public class ObjectImpl6 {
	public static void main(String[] args) throws CloneNotSupportedException {
		School1 school = new School1(); // 1000
		school.schoolName = "DAV School"; // 1000
		Student3 student1 = new Student3("Tom", 45, school);
		Student3 student2 = (Student3) student1.clone();
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