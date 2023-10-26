## DeSerialization

```java
/**
 * Implementation of DeSerialization  
 * Make sure the same version of pojo class need to use while reading data object from file.
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.Serialization;

import java.io.Serializable;
import java.io.*;

public class DeSerialization {
	public static void main(String args[]) {
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