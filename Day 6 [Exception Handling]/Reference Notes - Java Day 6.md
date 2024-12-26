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

- **Exception** is an event that disrupts the normal flow of a program.
- An exception is an abnormal condition.
- If a program gets abnormally terminated due to some abnormal condition, then that abnormal condition is known as an exception.

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instanceof-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">What is Exception</th>
    </tr>
</table>

---

## 2. Exception Handling

- **Exception Handling** is a mechanism used to handle exceptions. It allows defining an alternative path for program execution so that in case an exception occurs, the program does not abnormally terminate.

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instanceof-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">Exception Handling</th>
    </tr>
</table>

---

## 3. Error

- **Error** refers to an abnormal condition that we cannot handle. When such an error occurs, the program gets abnormally terminated.

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instanceof-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">Error</th>
    </tr>
</table>

---

## 4. Classification of Exception

### Checked Exception / Compile Time Exception

- Known as a compile-time exception.
- These exceptions occur due to access to resources outside of the JRE environment or inaccessible resources.
- Checked exceptions need to be handled using a try-catch block.

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instanceof-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">Checked Exception</th>
    </tr>
</table>

### Unchecked Exception / Runtime Exception

- Known as runtime exception.
- These exceptions are child classes of `RuntimeException`.
- These exceptions occur when the program fails or breaks unexpectedly due to incompatible code.

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instanceof-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">Unchecked Exception</th>
    </tr>
</table>

---

## 5. Exception Hierarchy

- **Exception Hierarchy**:
  - Throwable
    - Error
    - Exception
      - RuntimeException
      - IOException
      - SQLException
      - etc.

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instanceof-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">Exception Hierarchy</th>
    </tr>
</table>

---

## 6. Try with Multiple Catch

- The `try` block is used to enclose code that might throw an exception.
- If an exception occurs at a particular statement in the try block, the rest of the block code will not execute.
- Multiple `catch` blocks can be used to handle different types of exceptions.

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instanceof-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">Try with Multiple Catch</th>
    </tr>
</table>

---

## 7. Nested Try-Catch

- Nested `try-catch` blocks are used when one block might cause one error, and the entire block itself may cause another error.

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instanceof-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">Nested Try-Catch</th>
    </tr>
</table>

---

## 8. Finally Block

- The `finally` block always executes whether an exception is handled or not.
- It is used to define cleanup operations such as closing a file or releasing resources.
- Even if the program is terminated abruptly with `System.exit()`, the `finally` block will not execute.

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instanceof-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">Finally Block</th>
    </tr>
</table>

---

## 9. Some Useful Exception Classes

### NullPointerException

- This occurs when an application attempts to use `null` in a case where an object is required, such as calling a method on a `null` reference.

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instanceof-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">NullPointerException</th>
    </tr>
</table>

### NumberFormatException

- This occurs when an application tries to convert a string into a numeric type, but the string does not have the appropriate format.

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instanceof-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">NumberFormatException</th>
    </tr>
</table>

### ArrayIndexOutOfBoundsException

- This occurs when a program tries to access an array element with an invalid index.

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instanceof-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">ArrayIndexOutOfBoundsException</th>
    </tr>
</table>

### ArithmeticException

- This occurs when an exceptional arithmetic condition, like dividing by zero, occurs.

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instanceof-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">ArithmeticException</th>
    </tr>
</table>

---

## 10. Method Overriding in case of Exceptions

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

## 11. Exception Propagation

- Exception propagation is the process where an exception is thrown by one method and passed to the calling method. This continues until the exception is caught or it reaches the main method.

<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instanceof-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">Exception Propagation</th>
    </tr>
</table>
