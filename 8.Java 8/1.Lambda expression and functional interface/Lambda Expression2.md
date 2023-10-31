## Lambda Expression

### LambdaExpression2.java

```java
/**
 * Thread creation using Lambda expression
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.java8;

public class LambdaExpression2 {
    public static void main(String[] args) {
        Thread thread = new Thread(() -> {
            for (int i = 1; i <= 5; i++) {
                System.out.println("Thread: " + Thread.currentThread().getName() + " Count: " + i);
                try {
                    Thread.sleep(1000);
                } catch (InterruptedException e) {
                    e.printStackTrace();
                }
            }
        });
        thread.start();
    }
}

```
---
