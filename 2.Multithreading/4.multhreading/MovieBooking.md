## Multithreading - synchronization

### MovieBooking.java

```java
/**
 * synchronized method implementation.
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.thread4;

public class MovieBooking extends Thread {

	private static SeatBooking seatBooking;
	int seats;

	@Override
	public void run() {
		seatBooking.bookSeat(seats);
	}

	public static void main(String[] args) {
		seatBooking = new SeatBooking();
		MovieBooking thread1 = new MovieBooking();
		thread1.seats = 7;
		thread1.start();

		MovieBooking thread2 = new MovieBooking();
		thread2.seats = 5;
		thread2.start();
	}
}
```
---