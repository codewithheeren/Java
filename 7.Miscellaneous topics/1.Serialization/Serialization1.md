## Serialization

```java
/**
 * Implementation of Serialization  
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.Serialization;

import java.io.Serializable;
import java.io.*;

class Student implements Serializable {
	private int id;
	private String name;

	public Student(int id, String name) {
		this.id = id;
		this.name = name;
	}

	@Override
	public String toString() {
		return "Student [id=" + id + ", name=" + name + "]";
	}
}

public class Serialization {
	public static void main(String args[]) {
		try {
			Student s1 = new Student(211, "John");
			FileOutputStream fout = new FileOutputStream("file.txt");
			ObjectOutputStream out = new ObjectOutputStream(fout);
			out.writeObject(s1);
			out.flush();
			out.close();
			System.out.println("Data write in file successfully");
		} catch (Exception e) {
			System.out.println(e);
		}
	}
}
```
---