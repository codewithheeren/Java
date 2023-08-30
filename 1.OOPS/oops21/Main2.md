## OOPS - Scenerio where immutablity of class can break.

### Main2.java

```java

/** 
 * If The class holds the reference of another class(mutable object),
 * then we must implement deep copy while returning mutable object reference from immutable * class.
 * @author Heeren
 * @version 1.0
 */
package com.java.oops21;

final class ImmutableStudent {
	private final int id;
	private final String name;
	private final Address address;

	public ImmutableStudent(int id, String name, Address address) {
		this.name = name;
		this.id = id;
		this.address = address;
	}

	public int getId() {
		return id;
	}

	public String getName() {
		return name;
	}

	public Address getAddress() {
		return address;
	}
}

class Address {
	private String city;
	private String State;
	private int code;

	public String getCity() {
		return city;
	}

	public void setCity(String city) {
		this.city = city;
	}

	public String getState() {
		return State;
	}

	public void setState(String state) {
		State = state;
	}

	public int getCode() {
		return code;
	}

	public void setCode(int code) {
		this.code = code;
	}
}

public class Main2 {
	public static void main(String arg[]) {
		Address address = new Address();
		address.setCity("Moscow");
		address.setState("Xyz");
		address.setCode(12345);

		ImmutableStudent student = new ImmutableStudent(1, "Ram", address);
		System.out.println("Before modification: " + student.getAddress().getCode());
		student.getAddress().setCode(55555);
		System.out.println("After modification: " + student.getAddress().getCode());
	}
}

```
---
