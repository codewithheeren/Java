## Multithreading - synchronization

### MyThread1.java

```java
/**
 * synchronized block implementation.
 * same table object is shared by both threads.
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.thread5;

public class MyThread1 extends Thread {
	Table t;

	MyThread1(Table t) {
		this.t = t;
	}

	public void run() {
		t.printTable(5);
	}

}
```
---