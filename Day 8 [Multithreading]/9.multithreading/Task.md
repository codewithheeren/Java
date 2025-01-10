## Multithreading - Callable 

### Task.java

```java
/**
 * implementation of Callable interface
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.thread9;

import java.util.concurrent.Callable;

public class Task implements Callable {

	@Override
	public String call() throws Exception {
		System.out.println("Thread : " + Thread.currentThread().getName() + "starts");
		for (int i = 1; i <= 5; i++) {
			System.out.println(i);
		}
		System.out.println("Thread : " + Thread.currentThread().getName() + " ends");
		return "Task is done successfully";
	}
}
```
---