## Multithreading - Thread Creation

### CustomThread4.java

```java
/**
 * Thread creation using lambda expression
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.thread1;

public class CustomThread4 {
	public static void main(String[] args) {
		Thread thread = new Thread(() -> {
			for (int i = 1; i <= 5; i++) {
				System.out.println(Thread.currentThread().getName() + " execute - " + i + " times");
				try {
					Thread.sleep(500);
				} catch (InterruptedException e) {
					System.out.println(e);
				}
			}
		});
		thread.start();
	}
}
```
---