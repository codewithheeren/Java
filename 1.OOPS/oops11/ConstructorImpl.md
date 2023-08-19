## OOPS - Constructor 

### ConstructorImpl.java

```java
/**
 * Constructor Implementation : Non parameterize constructor
 * @author Heeren
 * @version 1.0
 */
package com.java.oops11;
public class ConstructorImpl{

	ConstructorImpl(){
    	System.out.println("Constructor invoke.");
    }

    public static void main(String[] args) {
        // Creating instances of the Person class using the constructor
    	ConstructorImpl object1 = new ConstructorImpl();
    	ConstructorImpl object2 = new ConstructorImpl();
    }
}
```
---