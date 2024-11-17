## OOPS - Method Overloading

### MethodOverlaoding1.java

```java
/**
 * Implementation of method overloading by changing no of parameters
 * @author Heeren
 * @version 1.0
 */
package com.java.oops6;
public class MethodOverlaoding1 {
	
	public void display(int num) {
        System.out.println("One parameter: " + num);
    }

    public void display(int num1, int num2) {
        System.out.println("Two parameters: " + num1 + ", " + num2);
    }

    public void display(int num1, int num2, int num3) {
        System.out.println("Three parameters: " + num1 + ", " + num2 + ", " + num3);
    }

    public static void main(String[] args) {
    	MethodOverlaoding1 example = new MethodOverlaoding1();
        example.display(5);
        example.display(10, 20);
        example.display(30, 40, 50);
    }

}
```
---