## OOPS - Static Import

### MathUtils.java

```java
package com.codewithheeren.java.oops8;

public class MathUtils {
    public static final double PI = 3.14159;

    public static double square(double number) {
        return number * number;
    }

    public static double cube(double number) {
        return number * number * number;
    }
}

```
---
### Main.java
```java
/**
 * static import 
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.java.oops9;
import static com.codewithheeren.java.oops8.MathUtils.*;
public class Main {
    public static void main(String[] args) {
        double radius = 5;
        double area = PI * square(radius);
        double volume = PI * cube(radius);

        System.out.println("Area of circle: " + area);
        System.out.println("Volume of sphere: " + volume);
    }
}
```
---