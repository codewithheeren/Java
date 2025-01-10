## Multithreading - Synchronization

### SeatBooking.java

```java
/**
 * synchronized method implementation.
 * data inconsistency
 * fix data inconsistency issue by making book seat method synchronized
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.thread4;

public class SeatBooking {
	private int totalSeats = 10;

	public synchronized void bookSeat(int requiredSeats) {

		if (totalSeats >= requiredSeats) {
			System.out.println("seats booked successfully");
			totalSeats = totalSeats - requiredSeats;
			System.out.println("seats available " + totalSeats);
		} else {
			System.out.println("required seats are not available");
			System.out.println("seats available " + totalSeats);
		}
	}
}
```
---