## OOPS - Interface 

### InterfaceImpl1.java

```java
/**
 * Interface
 * Dynamic Binding
 * media player can handle different types of media sources without being tied 
 * to a specific implementation, for that reason use Java interfaces.
 * @author Heeren
 * @version 1.0
 */
package com.java.oops16;

interface MediaPlayer {
	void play();

	void pause();

	void stop();
}

class MusicPlayer implements MediaPlayer {
	@Override
	public void play() {
		System.out.println("Playing music...");
	}

	@Override
	public void pause() {
		System.out.println("Pausing music...");
	}

	@Override
	public void stop() {
		System.out.println("Stopping music...");
	}
}

class VideoPlayer implements MediaPlayer {
	@Override
	public void play() {
		System.out.println("Playing video...");
	}

	@Override
	public void pause() {
		System.out.println("Pausing video...");
	}

	@Override
	public void stop() {
		System.out.println("Stopping video...");
	}
}

public class InterfaceImpl1 {
	public static void main(String[] args) {
		MediaPlayer musicPlayer = new MusicPlayer();
		MediaPlayer videoPlayer = new VideoPlayer();

		musicPlayer.play();
		musicPlayer.pause();
		musicPlayer.stop();

		videoPlayer.play();
		videoPlayer.pause();
		videoPlayer.stop();
	}
}
```
---