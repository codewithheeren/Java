## Multithreading - Synchronization

### Table.java

```java
/**
 * synchronized block implementation.
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.thread5;

class Table {
	void printTable(int n) {
		synchronized (this) {
			for (int i = 1; i <= 5; i++) {
				System.out.println(n * i);
				try {
					Thread.sleep(400);
				} catch (Exception e) {
					System.out.println(e);
				}
			}
		}
	}
}
```
---