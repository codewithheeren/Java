## Enum

```java
/**
 * Enum can have all attributes that a class can have like - constructor ,
 * static method,instance method,instance data member,static data member etc.
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.enum;
enum Season {
	WINTER(5), SPRING(10), SUMMER(15), FALL(20);
	//instance data memebers
	int temprature;
	static String countryName;
	//constructor
	private Season(int temprature) {
		this.temprature = temprature;
	}
	
	//instance method
	String printDetails() {
		return "Contry : "+countryName+"Temprature : "+temprature;
	}
	
	//static block
	static {
		countryName = "Russia";
	}
}

package com.codewithheeren.enum;
public class Enum6{

	public static void main(String args[]) {
		Season[] seasons = Season.values();
		for (Season season :seasons)
			System.out.println(season +" "+ season.printDetails());
	}
}

```
---
