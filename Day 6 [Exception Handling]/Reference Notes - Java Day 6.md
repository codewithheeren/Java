## Day 6 [Exception Handling]

## Topics Covered
1. [What is Exception](#1-what-is-Exception)
2. [Classification of Exception](#2-classification-of-Exception)
3. [Exception Hierarchy](#3-exception-hierarchy)
4. [Try Catch Blocks](#4-try-catch-blocks)
5. [Finally Block](#5-finally-block)
6. [Method Overriding in case of Exceptions](#6-method-overriding-in-case-of-exceptions)
7. [Exception Propagation](#7-exception-propagation)
8. [TryWithResource](#8-trywithresource)
9. [Custom Exceptions](#9-custom-exceptions)
10. [Assignment](#10-assignment)

---

## 1. What is Exception
<table>
    <tr>
        <td><a href="https://youtu.be/GkM-s_1UF4E">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">What is Exception</th>
    </tr>
</table>

🔵 what is Abnormal Termination of a program ?         
🔵**Exception**     
- is an event that disrupts the normal flow of a program.
- An exception is an abnormal condition.
- If a program gets abnormally terminated due to some abnormal condition, then that abnormal condition is known as an exception.

🔵**Exception Handling**    

Exception Handling is a mechanism used to handle exceptions. It allows defining an alternative path for program execution so that in case an exception occurs, the program does not abnormally terminate.

🔵 **Error**     
- Abnormal condition which we cannot handle and program gets abnormally terminates that abnormal condition become error.

## 2. Classification of Exception
<table>
    <tr>
        <td><a href="https://youtu.be/SVu8R-Ai1O0">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">Checked and Unchecked Exceptions</th>
    </tr>
</table>

🔵 **Checked Exception / Compile Time Exception**

- Known as compile time exception
- Any exception that occurs due to access to some resource outside of JRE environment or outside resource can’t be accessed or not available, then it is a checked exception
- Checked exception needs to be handled using try-catch block

🔵 **Unchecked Exception / Runtime Exception**

- Known as runtime exception
- Childs of RuntimeException class
- Code fail, not compatible, not complete or break in the programs, then it is an unchecked exception

## 3. Exception Hierarchy

<table>
    <tr>
        <td><a href="https://youtu.be/FLHqtHUh9YA">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">Exception Hierarchy</th>
    </tr>
</table>

![exceptions](https://github.com/codewithheeren/Java/assets/87074236/c76209f0-8896-4e2a-939b-ce2e66e206e8) 
   
🔵**Null Pointer Exception**

- When a variable is accessed which is not pointing to any object and refers to nothing or null.
- EG.-
`String str = null;`    
`System.out.println(str.length());` 

🔵**Number Format Exception**

- When an attempt is made to convert a string with improper format into a numeric value    
- EG.-    
`String invalidNumber = "abc";`      
`int num = Integer.parseInt(invalidNumber);`   

🔵**Array Index Out of Bounds Exception**
- If a program tries to access an array index that is negative, greater than, or equal to the length of the array.    
- EG.-     
`int[] numbers = {1, 2, 3};`      
`int outOfBounds = numbers[5];`    

🔵**Arithmetic Exception**

- When an attempt is made to divide two numbers and the number in the denominator is zero.    
- EG.-     
`int dividend = 10;`   
`int divisor = 0;`     
`int result = dividend / divisor;`

🔵**Difference between classnotfound exception and no class definition found error**     
**ClassNotFoundException:**   
Occurs when the programmer tries to dynamically load a class using Class.forName(), ClassLoader.loadClass(), or similar methods, but the class is not found in the classpath.

**NoClassDefFoundError:**     
Occurs when the JVM or a classloader tries to load a class that was available at compile-time but cannot be found at runtime, often due to missing or misconfigured class files.

## 4.Try Catch Blocks
<table>
    <tr>
        <td><a href="https://youtu.be/4OWq7vPRll8">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">Try Catch block</th>
    </tr>
</table>

🔵 **Try Block**
- try block is used to enclose the code that might throw an exception. It must be used within the method.
- If an exception occurs at the particular statement in the try block, the rest of the block code will not execute. So, it is recommended not to keep the code in try block that will not throw an exception.
- try block must be followed by either catch or finally block.
- Can have try block without catch block

🔵 **Catch Block**

- catch block is used to handle the Exception by declaring the type of exception within the parameter.
- The declared exception must be the parent class exception (i.e., Exception) or the generated exception type. However, the good approach is to declare the generated type of exception.
- catch block must be used after the try block only. You can use multiple catch blocks with a single try block.

🔵 **Try with Multiple Catch**

- We can define multiple catch blocks after a single try block.
- When using catch blocks for exceptions, need to handle child exceptions first before parent exception or specific exception before general exception to avoid unreachable code errror.

 🔵 **Nested Try-Catch**

- When we define a try block in another try block, it is a nested try-catch.
- Sometimes a situation may arise where a part of a block may cause one error and the entire block itself may cause another error. In such cases, exception handlers have to be nested.

## 5. Finally Block
<table>
    <tr>
        <td><a href="https://youtu.be/s_i6BxbcUUs">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">Finally Block</th>
    </tr>
</table>

- Define after the last catch block.   
- Will contain some important code which must need to execute.   
- Finally block always executes whether the exception is handled or not.   
- Is used to define cleanup operations such as used to close a connection or a file.
- 3 cases for finally block: 
  - try catch block success, finally executed
  - try success, catch fail, finally executed
  - try catch fail, finally executed

🔵 **Is there any condition when the finally block not get executed?**      
  - Yes, when abnormal program termination or a call from the system such as the use of System.exit();
    
🔵 **System.exit();**     
- When use this code System.exit(); then program terminates immediately.      

🔵 **Difference between final,finally and finalize method**      
**final Keyword:**     
Used to declare constants, prevent method overriding, and inheritance.     
**finally Block:**     
Used to execute important code such as cleanup actions that must be executed whether or not an exception is thrown.    
**finalize Method:**    
Called by the garbage collector before an object is destroyed to perform cleanup tasks.    
    
## 6. Method Overriding in case of Exceptions
<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instanceof-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e4" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">Method Overriding in case of Exceptions</th>
    </tr>
</table>

- parent method in throwing an Exception which is parent of Child method's exception.
      
**In case of Compiletime Exception**      
- If the Parent clas method does not declare an exception then child class overridden method cannot declare the checked/compiletime exception but still it can declare unchecked exception.
- If the Parent method declares an exception then child class overridden method can declare the same exception or child exception type or no exception but cannot declare parent exception type.

**In case of Runtime Exception**   
- In runtime exception for method overriding, exception hierarchy do not matter   
  - Parent throw arithmetic exception, child throw runtime exception--- work
  - Parent throw runtime exception, child throw arithmetic exception -- work
  - Parent not throw any exception, child throw exception ---- work
  - Parent throw exception, child not throw exception -- work


## 7. Exception Propagation

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instanceof-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e4" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">Exception Propagation</th>
    </tr>
</table>

Exception propagation is the process where an exception is thrown by one method and passed to the calling method. This continues until the exception is caught or it reaches the main method.  

## 8. TryWithResource

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instanceof-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e4" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">TryWithResource</th>
    </tr>
</table>

🔵 A feature in Java that automatically closes resources (like files or database connections) after they are no longer needed, without needing explicit finally blocks.      
🔵 It simplifies code by ensuring resources are closed even if an exception occurs.     
🔵 With try-with-resources, the need for a finally block to explicitly close resources is reduced, as it automatically handles resource closing. However, a finally block is still useful for handling additional cleanup tasks or for code that doesn't involve resources managed by the try-with-resources statement.

## 9. Custom Exceptions
<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instanceof-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e4" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">Custom Exceptions</th>
    </tr>
</table>

🔵 Custom exceptions are user-defined exceptions in Java, created by extending the Exception or RuntimeException class, to handle specific error scenarios that are not covered by standard exceptions.    
🔵 They help make code more readable and maintainable by providing clear and meaningful error messages tailored to the application’s needs.

---

## 10. Assignment   

**Task 1:** **Custom Exception for Bank Transactions**        
Create a BankAccount class with methods withdraw(double amount) and deposit(double amount). Throw a custom exception InsufficientFundsException if the withdrawal amount exceeds the balance. Handle the exception in the main method and display an appropriate error message.

**Task 2:** **Exception Propagation in a Travel Booking System**      
Write a program to simulate a travel booking system where:     
A method bookTicket() calls checkAvailability(), which throws a custom exception SeatsNotAvailableException.     
Show how the exception propagates through the call stack using throws. 

**Task 3:** **Design and implement a backend task scheduler for executing multiple tasks sequentially.**     
The scheduler must handle failures gracefully and incorporate retry logic for error-prone tasks. This task focuses on backend concepts such as exception handling, logging, and retry mechanisms to ensure the scheduler's robustness in a real-world application.    

**Task 4: Transaction Rollback in Banking System**    
Simulate a banking transaction where:       
If any step in the process (e.g., debit, credit) fails, throw a TransactionException.      
Use exception handling to rollback all completed steps to maintain consistency.       
Log the failure and provide feedback to the user.        

**Solution Task 3 -**

```java
import java.util.ArrayList;
import java.util.List;

// Custom exception to simulate task failures
class TaskExecutionException extends Exception {
    public TaskExecutionException(String message) {
        super(message);
    }
}

// Task class representing individual tasks
class Task {
    private final String taskName;
    private final boolean fail; // Indicates if the task should fail (for simulation)

    public Task(String taskName, boolean fail) {
        this.taskName = taskName;
        this.fail = fail;
    }

    public String getTaskName() {
        return taskName;
    }

    public void execute() throws TaskExecutionException {
        if (fail) {
            throw new TaskExecutionException("Simulated failure for task: " + taskName);
        }
        System.out.println("Task executed successfully: " + taskName);
    }
}

// Scheduler class to manage tasks
class TaskScheduler {
    private final List<Task> tasks;

    public TaskScheduler() {
        tasks = new ArrayList<>();
    }

    public void addTask(Task task) {
        tasks.add(task);
    }

    public void executeAllTasks() {
        for (Task task : tasks) {
            System.out.println("Starting task: " + task.getTaskName());
            int retries = 3;
            boolean success = false;

            for (int attempt = 1; attempt <= retries; attempt++) {
                try {
                    task.execute();
                    success = true;
                    break; // Exit the retry loop on success
                } catch (TaskExecutionException e) {
                    System.err.println("Attempt " + attempt + " failed for task: " + task.getTaskName());
                    System.err.println("Error: " + e.getMessage());
                    if (attempt < retries) {
                        try {
                            Thread.sleep(1000); // Delay between retries
                        } catch (InterruptedException ie) {
                            Thread.currentThread().interrupt(); // Restore interrupted status
                        }
                    }
                }
            }

            if (!success) {
                System.err.println("Task FAILED after " + retries + " attempts: " + task.getTaskName());
            } else {
                System.out.println("Task completed successfully: " + task.getTaskName());
            }

            System.out.println("--------------------------");
        }
    }
}

// Main class to test the scheduler
public class TaskSchedulerDemo {
    public static void main(String[] args) {
        TaskScheduler scheduler = new TaskScheduler();

        // Add tasks to the scheduler
        scheduler.addTask(new Task("Task 1", false)); // Success
        scheduler.addTask(new Task("Task 2", true));  // Fails
        scheduler.addTask(new Task("Task 3", true));  // Fails
        scheduler.addTask(new Task("Task 4", false)); // Success

        // Execute all tasks
        scheduler.executeAllTasks();
    }
}


```

**Solution Task 4 -**     

```java
// Custom exception for transaction failures
class TransactionException extends Exception {
    public TransactionException(String message) {
        super(message);
    }
}

class BankAccount {
    private final String accountNumber;
    private double balance;

    public BankAccount(String accountNumber, double initialBalance) {
        this.accountNumber = accountNumber;
        this.balance = initialBalance;
    }

    public String getAccountNumber() {
        return accountNumber;
    }

    public double getBalance() {
        return balance;
    }

    public void debit(double amount) throws TransactionException {
        if (amount <= 0) {
            throw new TransactionException("Debit amount must be positive.");
        }
        if (balance < amount) {
            throw new TransactionException("Insufficient funds for debit.");
        }
        balance -= amount;
        System.out.println("Debited: " + amount + ", New Balance: " + balance);
    }

    public void credit(double amount) throws TransactionException {
        if (amount <= 0) {
            throw new TransactionException("Credit amount must be positive.");
        }
        balance += amount;
        System.out.println("Credited: " + amount + ", New Balance: " + balance);
    }

    public void rollbackDebit(double amount) {
        balance += amount;
        System.out.println("Rolled back debit of: " + amount + ", Restored Balance: " + balance);
    }

    public void rollbackCredit(double amount) {
        balance -= amount;
        System.out.println("Rolled back credit of: " + amount + ", Restored Balance: " + balance);
    }
}

class TransactionProcessor {
    public static void processTransaction(BankAccount sender, BankAccount receiver, double amount) {
        System.out.println("Starting transaction: Transfer " + amount + " from " + sender.getAccountNumber() + " to " + receiver.getAccountNumber());

        try {
            // Step 1: Debit sender account
            sender.debit(amount);

            // Simulate failure after debit (for testing consistency)
            if (amount > 1000) {
                throw new TransactionException("Simulated failure: Amount exceeds limit.");
            }

            // Step 2: Credit receiver account
            receiver.credit(amount);

            System.out.println("Transaction completed successfully.");
        } catch (TransactionException e) {
            System.err.println("Transaction failed: " + e.getMessage());

            // Rollback changes to maintain consistency
            System.out.println("Initiating rollback...");
            sender.rollbackDebit(amount); // Rollback sender's debit
            // No need to rollback receiver's credit since it wasn't completed
        }
    }
}

public class BankingTransactionSimulation {
    public static void main(String[] args) {
        BankAccount sender = new BankAccount("S12345", 2000);
        BankAccount receiver = new BankAccount("R67890", 1000);

        // Test a successful transaction
        TransactionProcessor.processTransaction(sender, receiver, 500);

        System.out.println("-------------------------");

        // Test a failed transaction
        TransactionProcessor.processTransaction(sender, receiver, 1500);
    }
}
```
