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

---

## 1. What is Exception
<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instanceof-video">
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
        <td><a href="https://youtu.be/link-to-instanceof-video">
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
        <td><a href="https://youtu.be/link-to-instanceof-video">
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

🔵**Difference between classnotfound exception and no class definition not found error**     
**ClassNotFoundException:**   
Occurs when the programmer tries to dynamically load a class using Class.forName(), ClassLoader.loadClass(), or similar methods, but the class is not found in the classpath.

**NoClassDefFoundError:**     
Occurs when the JVM or a classloader tries to load a class that was available at compile-time but cannot be found at runtime, often due to missing or misconfigured class files.

## 4.Try Catch Blocks
<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instanceof-video">
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
        <td><a href="https://youtu.be/link-to-instanceof-video">
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
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">Method Overriding in case of Exceptions</th>
    </tr>
</table>

- There should be a parent to child relationship for exception hierarchy 
- Ex:
- If the superclass method does not declare an exception, subclass overridden method cannot declare the checked exception but it can declare unchecked exception.
- If the superclass method declares an exception, subclass overridden method can declare the same, subclass exception or no exception but cannot declare parent exception.

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
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">Exception Propagation</th>
    </tr>
</table>

Exception propagation is the process where an exception is thrown by one method and passed to the calling method. This continues until the exception is caught or it reaches the main method.  

## 8. TryWithResource

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instanceof-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
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
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">Custom Exceptions</th>
    </tr>
</table>

🔵 Custom exceptions are user-defined exceptions in Java, created by extending the Exception or RuntimeException class, to handle specific error scenarios that are not covered by standard exceptions.    
🔵 They help make code more readable and maintainable by providing clear and meaningful error messages tailored to the application’s needs.

