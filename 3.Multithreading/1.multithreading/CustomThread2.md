## Multithreading - Thread Creation

### CustomThread2.java

```java
/**
 * Thread creation using Runnable interface
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.thread1;

class CustomThread2 implements Runnable {
	public void run() {
		for (int i = 0; i <= 10; i++) {
			System.out.println(Thread.currentThread().getName() + " " + i + " time : is running...");
			try {
				Thread.sleep(500);
			} catch (InterruptedException e) {
				e.printStackTrace();
			}
		}
	}

	public static void main(String args[]) throws InterruptedException {
		Thread t1 = new Thread(new CustomThread2(), "Custom thread1");
		t1.start();

		Thread t2 = new Thread(new CustomThread2(), "Custom thread2");
		t2.start();
		// we can't run same thread twice.
		// t1.start(); //java.lang.IllegalThreadStateException
	}
}
```
---