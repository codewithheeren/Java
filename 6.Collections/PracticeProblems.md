### Collection Problems - 
```java
Collections class methods:
Collections.unmodifiableCollection()
Collections.reverse()
Collections.sort(listobj,comp0bj)
Collections.reverseOrder()
```
---	

### Problem 1: Given an array of integers, count the occurrences of each integer and store them in a map.

**Input:** int[] nums = {1, 2, 3, 2, 1, 3, 4, 5};
**Output:** {1=2, 2=2, 3=2, 4=1, 5=1}

### Problem 2: Find all duplicate elements in an array.

**Input:** int[] nums = {1, 2, 3, 2, 1, 3, 4, 5};
**Output:** [1, 2, 3]

### Problem 3: Iterate collection using list iterator and iterator ? also add and remove elements in list ?

**Input:** arraylist object - [3, 7, 1, 9, 5]
**Output:** remove 7 and add 10 after 1 - [3,1,10,9,5]

### Problem 4: How to short map basis on values ?

**Input:** { "apple" => 3, "banana" => 7, "cherry" => 1, "date" => 9, "fig" => 5 }
**Output:** { "cherry" => 1, "apple" => 3, "fig" => 5, "banana" => 7, "date" => 9 }

### Problem 5:  Remove all duplicates from the list collection ?

**Input:** An array input: [2, 4, 3, 2, 6, 4, 8, 10, 3]
**Output:** Expected Output: [2, 4, 3, 6, 8, 10]

### Problem 6: 
1. **Create an `Employee` class with attributes:**
    - `int employeeId`: A unique employee ID for each employee.
    - `String name`: The name of the employee.
    - `String department`: The department in which the employee works.
    - `double salary`: The salary of the employee.

2. **Override the `equals()` and `hashCode()` methods in the `Employee` class to ensure that employee objects are considered equal if their `employeeId` attributes are the same.

3. **Implement a `Main` class with a `main()` method where you:**
    - Instantiate a `HashSet` of `Employee` objects.
    - Create several `Employee` instances and add them to the `HashSet`.
    - Demonstrate the use of the `HashSet` by finding, removing, and checking for the existence of employees.
    - Display the number of employees in the `HashSet.

