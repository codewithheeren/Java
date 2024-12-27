# Exception Handling

## Topics Covered
1. [What is Exception](#1-what-is-exception)
2. [Exception Handling](#2-exception-handling)
3. [Error](#3-error)
4. [Classification of Exception](#4-classification-of-exception)
   - [Checked Exception](#checked-exception--compile-time-exception)
   - [Unchecked Exception](#unchecked-exception--runtime-exception)
5. [Exception Hierarchy](#5-exception-hierarchy)
6. [Try with Multiple Catch](#6-try-with-multiple-catch)
7. [Nested Try-Catch](#7-nested-try-catch)
8. [Finally Block](#8-finally-block)
9. [Some Useful Exception Classes](#9-some-useful-exception-classes)
   - [NullPointerException](#nullpointerexception)
   - [NumberFormatException](#numberformatexception)
   - [ArrayIndexOutOfBoundsException](#arrayindexoutofboundsexception)
   - [ArithmeticException](#arithmeticexception)
10. [Method Overriding in case of Exceptions](#10-method-overriding-in-case-of-exceptions)
11. [Exception Propagation](#11-exception-propagation)
12. [Difference between throws and throw keyword](#12-difference-between-throws-and-throw-keyword)
13. [Difference between final, finally and finalize method](#13-difference-between-final-finally-and-finalize-method)
14. [Difference between ClassNotFoundException and NoClassDefFoundError](#14-difference-between-classnotfoundexception-and-noclassdeffounderror)
15. [TryWithResource](#15-trywithresource)
16. [Custom Exceptions](#16-custom-exceptions)

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

🔵 **Runtime Exception**    
🔵 **Exception Handling in Method overriding**   

  - In runtime exception for method overriding, exception hierarchy do not matter
  - Parent throw arithmetic exception, child throw runtime exception--- work
  - Parent throw runtime exception, child throw arithmetic exception -- work
  - Parent not throw any exception, child throw exception ---- work
  - Parent throw exception, child not throw exception -- work

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

- The `try` block is used to enclose code that might throw an exception.
- If an exception occurs at a particular statement in the try block, the rest of the block code will not execute.
- Multiple `catch` blocks can be used to handle different types of exceptions.

 🔵 **Nested Try-Catch**

- Nested `try-catch` blocks are used when one block might cause one error, and the entire block itself may cause another error.

## 5. Finally Block
<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instanceof-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">Finally Block</th>
    </tr>
</table>

- The `finally` block always executes whether an exception is handled or not.
- It is used to define cleanup operations such as closing a file or releasing resources.
- Even if the program is terminated abruptly with `System.exit()`, the `finally` block will not execute.

## 6. Method Overriding in case of Exceptions

- In method overriding, the subclass can override the exception handling mechanism of the parent class. However, the overriding method cannot throw more exceptions than the method it overrides.

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instanceof-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">Method Overriding in case of Exceptions</th>
    </tr>
</table>

---

## 7. Exception Propagation

Exception propagation is the process where an exception is thrown by one method and passed to the calling method. This continues until the exception is caught or it reaches the main method.    

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instanceof-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">Exception Propagation</th>
    </tr>
</table>
