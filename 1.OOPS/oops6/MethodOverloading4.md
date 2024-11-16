## OOPS - Type permotion

### MethodOverloading4.java

```java
/**
 * Implementation of Type permotion
 * @author Heeren
 * @version 1.0
 */
package com.java.oops6;
public class MethodOverloading4 {
	
	public void display(int num1,double num2) {
        System.out.println("int and float");
    }
	public void display(double num1,int num2) {
        System.out.println("float and int");
    }
	
    public static void main(String[] args) {
    	MethodOverloading4 example = new MethodOverloading4();
    	example.display(10,10.0);
    }
}
```
---
