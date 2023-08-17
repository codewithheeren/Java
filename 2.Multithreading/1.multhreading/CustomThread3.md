## Multithreading - Thread Creation

### CustomThread3.java

```java
/**
 * Thread creation using anonymous class
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.thread1;

class CustomThread3 {
	public static void main(String args[]) throws InterruptedException {
		Thread thread = new Thread(new Runnable() {
			public void run() {
				for (int i = 1; i <= 5; i++) {
					System.out.println(Thread.currentThread().getName() + " " + i + " time : is running...");
					try {
						Thread.sleep(500);
					} catch (InterruptedException e) {
						e.printStackTrace();
					}
				}
			}
		}, "My Thread");
		thread.start();
	}
}
//Thread thread = new Thread(runnable,"Custom Thread");

```
---