## OOPS Day 6

 @author Heeren

 **Topics Covered**
--------------
### Exception Handling
- What is Exception
- Exception Handling
- Error
- Classification of Exception
	- Checked Exception  
	- Unchecked Exception
- Exception Hierarchy
- Try with Multiple Catch
- Nested Try-Catch
- Finally Block
- Some Usefule Exception Classes - NullPointerException, NumberFormatException, NumberFormatException, ArrayiIndexOutOfBoundsException, ArithmeticException
- Method overriding in case of exceptions
- Exception Propagation
- Difference between throws and throw keyword
- Difference between final,finally and finalize method
- Difference between classnotfound exception and no class definition not found error
- TryWithResource
- Custom Exceptions

--------------
### Abnormal Termination

### Exception

- Is an event that disrupts the normal flow of program
- Exception is an abnormal condition
- If a program gets abnormally terminated due to some abnormal condition, then that abnormal condition is known as an exception

### Exception Handling

- A mechanism uses to handle exceptions using which we define an alternative path for our program execution so that in case an exception occurs, then the program will not abnormally terminate.

### Error

- Abnormal condition which we cannot handle and program gets abnormally terminates that abnormal condition become error.

### Exception Hierarchy   

![exceptions](https://github.com/codewithheeren/Java/assets/87074236/c76209f0-8896-4e2a-939b-ce2e66e206e8)  

### Classification of Exception

### Checked Exception / Compile Time Exception

- Known as compile time exception
- Any exception that occurs due to access to some resource outside of JRE environment or outside resource can’t be accessed or not available, then it is a checked exception
- Checked exception needs to be handled using try-catch block

### Unchecked Exception / Runtime Exception

- Known as runtime exception
- Childs of RuntimeException class
- Code fail, not compatible, not complete or break in the programs, then it is an unchecked exception

### Try Block

- try block is used to enclose the code that might throw an exception. It must be used within the method.
- If an exception occurs at the particular statement in the try block, the rest of the block code will not execute. So, it is recommended not to keep the code in try block that will not throw an exception.
- try block must be followed by either catch or finally block.
- Can have try block without catch block

### Catch Block

- catch block is used to handle the Exception by declaring the type of exception within the parameter.
- The declared exception must be the parent class exception (i.e., Exception) or the generated exception type. However, the good approach is to declare the generated type of exception.
- catch block must be used after the try block only. You can use multiple catch blocks with a single try block.

### Multi-Catch Block

- Multiple catch blocks after a single try block
- When using catch blocks for exceptions, need to put child exception first before parent exception or specific exception before general exception to avoid unreachable code

### Nested Try-Catch

- When we define a try block in another try block, it is a nested try-catch
- Sometimes a situation may arise where a part of a block may cause one error and the entire block itself may cause another error. In such cases, exception handlers have to be nested.

### Finally Block

- Define after the last catch block
- Will contain some important code which must need to execute
- Finally block always executes whether the exception is handled or not
- Is used to define cleanup operations such as used to close a connection or a file.
- 3 cases for finally block: 
  - try catch block success, finally executed
  - try success, catch fail, finally executed
  - try catch fail, finally executed

### Interview Question

- Is there any condition when the finally block not get executed?
  - Yes, when abnormal program termination or a call from the system such as the use of System.exit();

**System.exit();**

- When use this code System.exit(); then program termination

### Exception Handling with Method Overriding

- There should be a parent to child relationship for exception hierarchy 
  - Ex:
    - If the superclass method does not declare an exception, subclass overridden method cannot declare the checked exception but it can declare unchecked exception.
    - If the superclass method declares an exception, subclass overridden method can declare the same, subclass exception or no exception but cannot declare parent exception.

### Runtime Exception

- In runtime exception for method overriding, exception hierarchy do not matter
  - Parent throw arithmetic exception, child throw runtime exception--- work
  - Parent throw runtime exception, child throw arithmetic exception -- work
  - Parent not throw any exception, child throw exception ---- work
  - Parent throw exception, child not throw exception -- work

### Null Pointer Exception

- When a variable is accessed which is not pointing to any object and refers to nothing or null

### Number Format Exception

- When an attempt is made to convert a string with improper format into a numeric value

### Array Index Out of Bounds Exception

- If a program tries to access an array index that is negative, greater than, or equal to the length of the array

### Arithmetic Exception

- When an attempt is made to divide two numbers and the number in the denominator is zero

### Normal Termination
