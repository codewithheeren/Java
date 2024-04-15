## OOPS - Achiving 100% immutablity by creating clong in constructor as well.

### Main4.java

```java

/** 
 * Deep Cloning to protect Immutablity by also having cloning in constructor
 * @author Heeren
 * @version 1.0
 */
package com.java.oops21;
```java
final class ImmutableStudent {
	private final int id;
	private final String name;
	private final Address address;

	public ImmutableStudent(int id, String name, Address address) throws CloneNotSupportedException {
		this.name = name;
		this.id = id;
		this.address = (Address) address.clone();
	}

	public int getId() {
		return id;
	}

	public String getName() {
		return name;
	}

	public Address getAddress() throws CloneNotSupportedException {
		return (Address) address.clone();
	}

	@Override
	public String toString() {
		return "ImmutableStudent [id=" + id + ", name=" + name + ", address=" + address + "]";
	}

}

class Address implements Cloneable {
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

	public Object clone() throws CloneNotSupportedException {
		return super.clone();
	}

	@Override
	public String toString() {
		return "Address [city=" + city + ", State=" + State + ", code=" + code + "]";
	}
}

public class Main3 {
	public static void main(String arg[]) throws CloneNotSupportedException {
		Address address = new Address();
		address.setCity("Random-city-name");
		address.setState("state-name");
		address.setCode(12345);

		ImmutableStudent student = new ImmutableStudent(1, "Ram", address);
		System.out.println("Before modification: " + student.getAddress().getCode());
		student.getAddress().setCode(55555);
		System.out.println("After modification: " + student.getAddress().getCode());
		address.setCode(99999);
		System.out.println("After modification from old address object reference " + student);
	}
}
```
