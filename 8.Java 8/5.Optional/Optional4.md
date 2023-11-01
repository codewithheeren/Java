## Optional Implementation

### Optional4.java

```java
/**
 * Throwing an Exception if Value is Absent.
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.java8;

import java.util.Optional;

public class Optional4 {
    public static void main(String[] args) {
        int userId = 42; // Change this to an existing user ID to find the user

        Optional<User> optionalUser = findUserById(userId);
        User user = optionalUser.orElseThrow(() -> new UserNotFoundException("User not found"));

        // If the user is present, continue with user operations
        System.out.println("User found: " + user.getName());
    }

    public static Optional<User> findUserById(int userId) {
        // Simulate a method that finds a user by ID
        if (userId == 42) {
            return Optional.of(new User(42, "Alice"));
        } else {
            return Optional.empty();
        }
    }
}
```
---
### User.java
```java
class User {
    private int id;
    private String name;

    public User(int id, String name) {
        this.id = id;
        this.name = name;
    }

    public int getId() {
        return id;
    }

    public String getName() {
        return name;
    }
}
```
---
UserNotFoundException.java
```java
class UserNotFoundException extends RuntimeException {
    public UserNotFoundException(String message) {
        super(message);
    }
}
```
---
