/**
 * Implementation of static and instance data members
 * @author Heeren
 * @version 1.0
 */
package com.java.oops9;

//method overriding by changing access modifiers. 
//Default -> protected -> public 
class Base2 {
	protected void method() {
		System.out.println("Base Class : method()");
	}
}

class Child2 extends Base1 {
	public void method() {
		System.out.println("Child Class : method()");
	}
}

public class MethodOverriding3 {
	public static void main(String[] args) {
		Child2 child = new Child2();
		child.method();
	}
}
