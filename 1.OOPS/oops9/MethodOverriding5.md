/**
 * Implementation of static and instance data members
 * @author Heeren
 * @version 1.0
 */
package com.java.oops9;

//method Hiding
class Base4{
	static void method() {
	   System.out.println("Base Class : method()");
   }
}

class Child4 extends Base4{
	   static void method() {
		   System.out.println("Child Class : method()");
	   }
}

public class MethodOverriding5 {
	public static void main(String[] args) {
		Child4.method();
	}
}
