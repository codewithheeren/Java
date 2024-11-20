## OOPS - Composition

### CompositionMainClass.java

```java
/**
 * Implementation of Composition
 * @author Heeren
 * @version 1.0
 */
package com.java.oops8;

class Engine {
	String type;

	Engine(String type) {
		this.type = type;
	}

	@Override
	public String toString() {
		return "Engine{type='" + type + "'}";
	}
}

class Car {
	Engine engine;

	Car(String engineType) {
		this.engine = new Engine(engineType);
	}

	@Override
	public String toString() {
		return "Car{" + "engine=" + engine + '}';
	}
}

public class CompositionMainClass {
	public static void main(String[] args) {
		Car car = new Car("V8");
		System.out.println(car);
	}
}

```
---
