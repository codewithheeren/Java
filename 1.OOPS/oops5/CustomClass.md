/**
 * Implementation of static and instance data members
 * @author Heeren
 * @version 1.0
 */
package com.java.oops5;
// local variable and Data shadowing
class CustomClass {
	int x = 10;

	public void display() {
		int x = 20;
		System.out.println(x);
		System.out.println(this.x);
	}

	public static void main(String[] a) {
		CustomClass customClass = new CustomClass();
		customClass.display();
	}
}
