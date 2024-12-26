## OOPS - Custom Immutable class implementation

### Main1.java

```java

/**
 * Emmutable class implementation.
 * Rules to Create immutable class -
 * Class must be final 
 * Class data members must be private and final .
 * Do not define any setter method in that class.
 * Data members must initialize using constructor only. 
 * @author Heeren
 * @version 1.0
 */
package com.java.oops21;

public final class Person {
    private final String firstName;
    private final String lastName;
    private final int age;

    public Person(String firstName, String lastName, int age) {
        this.firstName = firstName;
        this.lastName = lastName;
        this.age = age;
    }

    public String getFirstName() {
        return firstName;
    }

    public String getLastName() {
        return lastName;
    }

    public int getAge() {
        return age;
    }

    @Override
    public String toString() {
        return "Person{" +
                "firstName='" + firstName + '\'' +
                ", lastName='" + lastName + '\'' +
                ", age=" + age +
                '}';
    }
}

```
---
