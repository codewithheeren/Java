## Exception Handling 

### ExceptionHandling12.java
```java
/**
 * UseCase 0 parent method in throwing an Exception which is parent of Child method's exception. 
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.exception;
import java.io.IOException;

class Superclass {
    public void readFile() throws Exception {
        System.out.println("Reading file in superclass");
        throw new IOException("IO Exception occurred");
    }
}

class Subclass extends Superclass {
    @Override
    public void readFile() throws ArithmeticException {
            System.out.println("Reading file in subclass");   
    }
}

public class ExceptionHandling12 {
    public static void main(String[] args) {
        Superclass obj = new Subclass();
        try {
            obj.readFile();
        }  catch (Exception e) {
			e.printStackTrace();
		}
    }
}
```

```java
/**
 * UseCase 1 parent method in throwing checked exception and child is not throwing any exception. 
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.exception;
import java.io.IOException;

class Superclass {
    public void readFile() throws IOException {
        System.out.println("Reading file in superclass");
        throw new IOException("IO Exception occurred");
    }
}

class Subclass extends Superclass {
    @Override
    public void readFile() {
        try {
            System.out.println("Reading file in subclass");
            super.readFile();
        } catch (IOException e) {
            System.out.println("Handled IOException in subclass: " + e.getMessage());
        }
    }
}

public class ExceptionHandling12 {
    public static void main(String[] args) {
        Superclass obj = new Subclass();
        try {
            obj.readFile();
        } catch (IOException e) {
            System.out.println("Caught IOException in main method: " + e.getMessage());
        }
    }
}

```
---
```java
/**
 * UseCase 2 parent method in throwing checked exception and child is throwing checked exception which is child class exception of parent thown exception class. 
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.exception;
import java.io.FileNotFoundException;
import java.io.IOException;

class Superclass {
    public void readFile() throws IOException {
        System.out.println("Reading file in superclass");
        throw new IOException("IO Exception occurred");
    }
}

class Subclass extends Superclass {
    @Override
    public void readFile() throws FileNotFoundException {
        try {
            System.out.println("Reading file in subclass");
            super.readFile();
        } catch (IOException e) {
            System.out.println("Handled IOException in subclass: " + e.getMessage());
        }
    }
}

public class ExceptionHandling12 {
    public static void main(String[] args) {
        Superclass obj = new Subclass();
        try {
            obj.readFile();
        } catch (IOException e) {
            System.out.println("Caught IOException in main method: " + e.getMessage());
        }
    }
}
```
---
```java
/**
 * UseCase 3 parent method in throwing any unchecked exception and child is throwing any unchecked exception , irrespective of their relationsship it will work. 
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.exception;

class Superclass {
    public void readFile() throws  ArithmeticException{
        System.out.println("Reading file in superclass");
        throw new ArithmeticException("IO Exception occurred");
    }
}

class Subclass extends Superclass {
    @Override
    public void readFile() throws RuntimeException {
        try {
            System.out.println("Reading file in subclass");
            super.readFile();
        } catch (RuntimeException e) {
            System.out.println("Handled IOException in subclass: " + e.getMessage());
        }
    }
}

public class ExceptionHandling12 {
    public static void main(String[] args) {
        Superclass obj = new Subclass();
        try {
            obj.readFile();
        } catch (RuntimeException e) {
            System.out.println("Caught IOException in main method: " + e.getMessage());
        }
    }
}
```
---
