## OOPS - Interface 

### InterfaceImpl2.java

```java
/**
 * Interface
 * one concrete class can implements multiple interfaces.
 * similarly One class can extends another class and implements another interface at same time.
 * @author Heeren
 * @version 1.0
 */
package com.java.oops16;
interface MusicalDevice {
    void playMusic();
    void pauseMusic();
    void stopMusic();
}

interface InternetConnectivity {
    void connectToInternet();
    void disconnectFromInternet();
}

class SmartDevice implements MusicalDevice, InternetConnectivity {
    @Override
    public void playMusic() {
        System.out.println("Playing music...");
    }

    @Override
    public void pauseMusic() {
        System.out.println("Pausing music...");
    }

    @Override
    public void stopMusic() {
        System.out.println("Stopping music...");
    }

    @Override
    public void connectToInternet() {
        System.out.println("Connecting to the internet...");
    }

    @Override
    public void disconnectFromInternet() {
        System.out.println("Disconnecting from the internet...");
    }
}

public class InterfaceImpl2{
    public static void main(String[] args) {
        SmartDevice smartDevice = new SmartDevice();

        smartDevice.playMusic();
        smartDevice.pauseMusic();
        smartDevice.stopMusic();

        smartDevice.connectToInternet();
        smartDevice.disconnectFromInternet();
    }
}
```
---