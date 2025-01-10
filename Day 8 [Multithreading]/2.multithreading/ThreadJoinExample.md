## Multithreading - Join method implementation

### ThreadJoin.java

```java
/**
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.thread2;

import java.io.*;

class ThreadJoin extends Thread {
	public void run() {
		for (int j = 1; j <= 5; j++) {
			try {
				Thread.sleep(300);
				System.out.println("The current thread: " + Thread.currentThread().getName() + " " + j + " times");
			} catch (Exception e) {
				System.out.println("The exception has been caught: " + e);
			}
		}
	}
}
```
---