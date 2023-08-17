## Multithreading - executor framework

### Executor2.java

```java
/**
 * implementation of executor framework
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.thread7;
 
public class Executor2 implements Runnable {
    private String name;
 
    public Executor2(String name) {
        this.name = name;
    }
 
    public void run() { 
        System.out.println("Start executing " + name);
        try {
            Thread.sleep(1000);
            System.out.println("Executing " + name);
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
        System.out.println("Finished execution " + name);
        System.out.println();
    } 
}
 
```
---