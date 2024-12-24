## OOPS - Interface 

### InterfaceImpl3.java

```java
/**
 * Multiple inheritance in case of interfaces.
 * @author Heeren
 * @version 1.0
 */
package com.java.oops16;

interface Device {
	void turnOn();
	void turnOff();
}

interface Connectivity {
	void connect();
	void disconnect();
}

interface Functionality {
	void performFunction();
}

interface SmartElectricDevice extends Device, Connectivity {
	void lowPowerConsumption();
}

class SmartLightBulb implements SmartElectricDevice {
	private boolean isOn = false;

	@Override
	public void turnOn() {
		isOn = true;
		System.out.println("Smart light bulb turned on.");
	}

	@Override
	public void turnOff() {
		isOn = false;
		System.out.println("Smart light bulb turned off.");
	}

	@Override
	public void connect() {
		System.out.println("Smart light bulb connected to the network.");
	}

	@Override
	public void disconnect() {
		System.out.println("Smart light bulb disconnected from the network.");
	}

	@Override
	public void lowPowerConsumption() {
		System.out.println("Consuming low power");

	}
}

public class InterfaceImpl3 {
	public static void main(String[] args) {
		SmartLightBulb smartBulb = new SmartLightBulb();
		smartBulb.lowPowerConsumption();
		smartBulb.turnOn();
		smartBulb.connect();
		smartBulb.disconnect();
		smartBulb.turnOff();
	}
}
```
---