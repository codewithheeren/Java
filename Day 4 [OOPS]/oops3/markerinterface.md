## OOPS - Marker Interface Implementation 

### Auditable.java

```java
/**
 * Marker Interface
 * @author Heeren
 * @version 1.0
 */

package com.codewithheeren.java.oops3;
public interface Auditable {
    // No methods or fields
}

```
---

### Product.java
```java
package com.codewithheeren.java.oops3;
public class Product {
    private String name;
    private double price;

    public Product(String name, double price) {
        this.name = name;
        this.price = price;
    }

    @Override
    public String toString() {
        return "Product{name='" + name + "', price=" + price + "}";
    }
}

```
---

### User.java
```java
package com.codewithheeren.java.oops3;
public class User implements Auditable {
    private String username;
    private String email;

    public User(String username, String email) {
        this.username = username;
        this.email = email;
    }

    @Override
    public String toString() {
        return "User{username='" + username + "', email='" + email + "'}";
    }
}

```
---

### AuditService.java
```java
package com.codewithheeren.java.oops3;
public class AuditService {
    public static void audit(Object obj) {
        if (obj instanceof Auditable) {
            System.out.println("Auditing changes to: " + obj);
            // Perform actual auditing logic here
        } else {
            System.out.println("No auditing required for: " + obj);
        }
    }

    public static void main(String[] args) {
        User user = new User("john_doe", "john.doe@example.com");
        Product product = new Product("Laptop", 999.99);

        audit(user);   // This should be audited
        audit(product); // This should not be audited
    }
}

```
---