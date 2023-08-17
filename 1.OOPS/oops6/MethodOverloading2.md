/**
 * Implementation of static and instance data members
 * @author Heeren
 * @version 1.0
 */
package com.java.oops6;
// method overloading by changing data types of parameters.
public class MethodOverloading2 {

    public int add(int a, int b) {
        return a + b;
    }

    public double add(double a, double b) {
        return a + b;
    }

    public double add(int a, double b) {
        return a + b;
    }

    public static void main(String[] args) {
    	MethodOverloading2 example = new MethodOverloading2();

        System.out.println("Sum of integers: " + example.add(5, 10));
        System.out.println("Sum of doubles: " + example.add(3.5, 2.7));
        System.out.println("Sum of int and double: " + example.add(8, 4.2));
    }
}
