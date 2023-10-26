## Java Serialization with Inheritance


```java
/**
 * If a class implements Serializable interface then all its sub classes will also be serializable.   
 * @author Heeren
 * @version 1.0
 */
 
package com.codewithheeren.Serialization;

import java.io.FileInputStream;
import java.io.FileOutputStream;
import java.io.ObjectInputStream;
import java.io.ObjectOutputStream;
import java.io.Serializable;

class Person implements Serializable {
	int personId;
	String personName;

	Person(int personId, String personName) {
		this.personId = personId;
		this.personName = personName;
	}

	@Override
	public String toString() {
		return "Person [personId=" + personId + ", personName=" + personName + "]";
	}
}

class Student extends Person {
	String courseName;
	int tuitionFee;

	public Student(int personId, String personName, String courseName, int tuitionFee) {
		super(personId, personName);
		this.courseName = courseName;
		this.tuitionFee = tuitionFee;
	}

	@Override
	public String toString() {
		return "Student [courseName=" + courseName + ", tuitionFee=" + tuitionFee + ", personId=" + personId
				+ ", personName=" + personName + "]";
	}

}

public class Serialization {
	public static void main(String args[]) {
		try {
			Student s1 = new Student(211, "Timmy", "Engineering", 9000);
			FileOutputStream fout = new FileOutputStream("file.txt");
			ObjectOutputStream out = new ObjectOutputStream(fout);
			out.writeObject(s1);
			out.flush();
			out.close();
			System.out.println("Data written in file successfully");
		} catch (Exception e) {
			System.out.println(e);
		}
		try {
			ObjectInputStream in = new ObjectInputStream(new FileInputStream("file.txt"));
			Student s = (Student) in.readObject();
			System.out.println(s);
			in.close();
		} catch (Exception e) {
			System.out.println(e);
		}
	}
}


```
---