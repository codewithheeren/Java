## Multithreading - Explicit calling of run() method

### CustomThread5.java

```java
/**
 * Calling Java run() method directly instead start() method.
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.thread1;

class CustomThread5 extends Thread {
	public void run() {
		for (int i = 1; i < 5; i++) {
			try {
				Thread.sleep(500);
			} catch (InterruptedException e) {
				System.out.println(e);
			}
			System.out.println(Thread.currentThread().getName() + " " + i);
		}
	}

	public static void main(String args[]) {
		CustomThread5 thread1 = new CustomThread5();
		CustomThread5 thread2 = new CustomThread5();
		//	 t1.start();  
		//	 t2.start();  
		thread1.run();
		thread2.run();
		// there is no context-switching because here t1 and t2 will be treated
		// as normal object not thread object.
	}
}
```
---