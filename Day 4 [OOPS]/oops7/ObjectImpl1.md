## OOPS - Object Class Implementations 

### ObjectImpl1.java

```java
/**
 * Object Class : ToString method implementation
 * Methods in object class-
 * toString
 * equals
 * hashCode
 * getClass
 * wait
 * notify
 * notifyAll
 * finalize
 * clone
 * @author Heeren
 * @version 1.0
 */
package com.java.oops19;

class Person {
    private String name;
    private int age;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    @Override
    public String toString() {
        return "Person{name='" + name + "', age=" + age + "}";
    }
}

public class ObjectImpl1 {
    public static void main(String[] args) {
        Person person = new Person("Alice", 30);
        System.out.println(person); // The toString() method is implicitly called here
    }
}
```
---