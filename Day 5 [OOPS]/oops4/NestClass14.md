## OOPS - Nested Class

### OuterClass.java

```java
/**
 * Inner Interface - Interface in a class   
 * @author Heeren
 * @version 1.0
 */
package com.java.oops20;
class OuterClass {
    public interface InnerInterface {
        void displayMessage();
    }

    public static void showGreeting() {
        System.out.println("Hello from OuterClass!");
    }
}


```
---

### NestClass14.java

```java

package com.java.oops20;
public class NestClass14 implements OuterClass.InnerInterface {
    @Override
    public void displayMessage() {
        System.out.println("Message from InnerInterface");
    }

    public static void main(String[] args) {
        OuterClass.showGreeting();
        NestClass14 innerInterface = new NestClass14();
        innerInterface.displayMessage();
    }
}

```
---