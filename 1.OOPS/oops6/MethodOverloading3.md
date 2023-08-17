/**
 * Implementation of static and instance data members
 * @author Heeren
 * @version 1.0
 */
package com.java.oops6;
//Type permotion
public class MethodOverloading3 {
	
	public void display(byte num) {
        System.out.println("One parameter byte type: " + num);
    }
	
	public void display(int num) {
        System.out.println("One parameter int type: " + num);
    }
	
	public void display(long num) {
        System.out.println("One parameter long type: " + num);
    }
	
	public void display(float num) {
        System.out.println("One parameter float type: " + num);
    }
	
	public void display(double num) {
        System.out.println("One parameter double type: " + num);
    }

    public static void main(String[] args) {
    	MethodOverloading3 example = new MethodOverloading3();
    	example.display(10);
    	example.display(10.5);
    }
}
