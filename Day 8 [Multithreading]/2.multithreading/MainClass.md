## Multithreading - Join method implementation

### MainClass.java

```java
/**
 * Join Method Implementation.
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.thread2;

public class MainClass {
	public static void main(String argvs[]) {
		ThreadJoin th1 = new ThreadJoin();
		ThreadJoin th2 = new ThreadJoin();
		ThreadJoin th3 = new ThreadJoin();
		th1.start();

		// starting the second thread after when  
		// the first thread th1 has ended or died.  
		try {
		//	System.out.println("The current thread: " + Thread.currentThread().getName());
			th1.join();
		} catch (Exception e) {
			System.out.println("The exception has been caught " + e);
		}

		th2.start();
		th3.start();
	}
}
```
---