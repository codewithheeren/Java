## OOPS - Nested Class

### OuterInterface.java

```java
/**
 * Inner Interface - Interface in another interface   
 * @author Heeren
 * @version 1.0
 */
package com.java.oops20;

interface OuterInterface {
    void outerMethod();

    interface InnerInterface {
        void innerMethod();
    }
}

```
---

### NestClass13.java

```java

package com.java.oops20;
public class NestClass13 implements OuterInterface, OuterInterface.InnerInterface {
    @Override
    public void outerMethod() {
        System.out.println("OuterInterface Method");
    }

    @Override
    public void innerMethod() {
        System.out.println("InnerInterface Method");
    }

    public static void main(String[] args) {
    	NestClass13 innerInterface = new NestClass13();
    	innerInterface.outerMethod();
    	innerInterface.innerMethod();
    }
}

```
---