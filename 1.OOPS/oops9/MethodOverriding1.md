/**
 * Implementation of static and instance data members
 * @author Heeren
 * @version 1.0
 */
package com.java.oops9;

//method overriding 
class Base {
	public void method() {
		System.out.println("Base Class : method()");
	}
}

class Child extends Base {
	public void method() {
		System.out.println("Child Class : method()");
	}
}

public class MethodOverriding1 {
	public static void main(String[] args) {
		Child child = new Child();
		child.method();
	}
}
