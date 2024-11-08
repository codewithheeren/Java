## OOPS - Coding Problems

```java
/**
 * java OOPS based Coding problems
 * @author Heeren
 */
**1**
Task 1: Implement a class with a static variable to count the number of instances and then Create multiple instances of this class and print the count.

Task 2: Develop a Java class to represent a library, with a static data member to store the total number of books in the library and an instance data member to store the book's title. Implement a static method to update the total count when a new book is added.

Task 3: Implement a Java class to manage a shopping cart, with an instance data member to store the items in the cart and instance methods to add, remove, and calculate the total price of the items.

Task 4: Develop a Java program to process a list of employees. Use instance methods to calculate their salary based on after 10% of tax deduction.

```
---
```java
**2**
Task 1: Implement different real time examples of following inheritances types Multilevel , hybrid , hierarchical.

Task 2: Do all use case of access modifiers with variables, methods and class.access them within same class , outside the class , within same package and outside the package using inheritance and association.

Task 3: Define a class Person with private attributes name and age. Provide public methods getName(), setName(), getAge(), and setAge() to access and modify these attributes using association from main class.

Task 4: Create a superclass Vehicle with a protected attribute speed. Create a subclass Car that inherits from Vehicle and has a method displaySpeed() to access and display the speed attribute.
        usecase 1 - create car class within same package. usecase 2 - create car class within other package

Task 5: Employee Management System: Build a system with classes Employee, Manager, Developer, and Intern. Implement inheritance where Manager and Developer inherit from Employee. Use method overriding for any specific 
        functionalities.

Task 6: Design classes for Customer, Product, Cart, and Order. Implement association where a Customer can add items to a Cart and place an Order.

Task 7: Build a system with classes Vehicle, Car, Truck, and RentalAgency. Implement inheritance and method overriding to handle rental operations for different vehicle types.

Task 8: Define classes for Contact, AddressBook, and Group. Use association to manage contacts in an address book and group them based on categories.

```
---
```java
**3**
Task 1: Develop a class Transaction with final attributes transactionId and amount. Implement multiple constructors for initializing transactions with different parameters (e.g., ID and amount, or just amount). Ensure that transactionId is set only once and print the transaction details for different transaction objects.

Task 2: Define a class Message with a final method sendMessage(). Implement a subclass EmailMessage that attempts to override sendMessage(). check the impact of the final keyword on method overriding. and similarly make class final and try to inherit that and also check the impact of final keyword on making class as final.

Task 3: Implement both types of association , one real time example of aggregation and one example of composition.Also make understanding with their diffeerences ?

Task 4: Access one class static property and functionality into another class using static import.

Task 5: Create a class Employee with attributes employeeId and salary. Implement a constructor that validates input parameters (e.g., positive salary) and throws an exception for invalid values.
 
```
---
```java
**4**
Task 1: Write a program that takes user input for name and age for user registration using the console only.   
Create a custom exception called InvalidAgeException which should be thrown if a user tries to register with an age less than 18.
 
Name Validation:    
Ensure that the name is not empty and does not contain any digits or special characters. If invalid, throw a custom exception called InvalidNameException.
Retry Mechanism: 
If the user provides invalid input (either invalid name or age), prompt the user to try again until valid input is provided.
Exit Option:  
If user dont want to continue, ask to user to press 'E' or 'e' to exit.

Task 2: Create a Java program that reads from a file and handles exceptions related to file I/O, such as FileNotFoundException and IOException.   
Additionally, use an anonymous class to filter files with a specific extension (e.g.,Only ".txt" file should be read other wise some customexception "FileNotAccepted" will throw).       
also display the contents of the filtered files.      
```
---
