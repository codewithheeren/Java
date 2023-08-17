## Multithreading - Thread Creation

### CustomThread1.java

```java
/**
 * Thread creation using Thread class
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.thread1;

class CustomThread1 extends Thread {
	public CustomThread1(String threadName) {
		super(threadName);
	}

	public void run() {
		for (int i = 0; i <= 10; i++) {
			System.out.println(Thread.currentThread().getName() + " " + i + "time : is running...");
			try {
				Thread.sleep(500);
			} catch (InterruptedException e) {
				e.printStackTrace();
			}
		}
	}

	public static void main(String args[]) {
		CustomThread1 thread = new CustomThread1("Custom Thread");
		thread.start();
		System.out.println(Thread.currentThread().getName());
	}
}
```
---