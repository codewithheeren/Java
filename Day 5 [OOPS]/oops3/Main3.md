## OOPS - Protecting immutability of immutable class

### Main3.java

```java

/** 
 * Deep Cloning to protect Immutablity
 * @author Heeren
 * @version 1.0
 */
package com.java.oops21;
final class ImmutableStudent 
{
    private final int id;
    private final String name;
    private final Address address;
    public ImmutableStudent(int id, String name, Address address) 
    {
        this.name = name;
        this.id = id;
        this.address = address;
    }
    public int getId() 
    {
        return id;
    }
    public String getName() 
    {
        return name;
    }
    public Address getAddress() throws CloneNotSupportedException
    {
        return (Address) address.clone();
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
}


public class Main3
{
    public static void main(String arg[]) throws CloneNotSupportedException
    {
        Address address = new Address();
        address.setCity("Random-city-name");
        address.setState("state-name");
        address.setCode(12345);
        
        ImmutableStudent student = new ImmutableStudent(1, "Ram", address);
        System.out.println("Before modification: "+ student.getAddress().getCode());
        student.getAddress().setCode(55555);
        System.out.println("After modification: "+ student.getAddress().getCode());
    }
}  



```
---
