## OOPS Day 10

 @author Heeren

 **Topics Covered**
--------------
- Arrays vs collection
- Collection hierarchy
- List
- Arraylist
- Linked list
- Vector
- Vector vs ArrayList
- Stack
- Diffence between arraylist and list
- Cursor
  - iterator
  - List iterator
- Set
- Hashset
- linkedhashset
- Sortedset
- Treeset
- Comparable vs comparator
---
**Collection Framework**

**Array vs Collection**

**Array**

  - Fix in size
  - Arrays can hold only the same type of data i.e only homogeneous data types elements are allowed in arrays.
  - Do not implement any data structure.
  - Arrays can hold both object and primitive type data.

**Collection**

  - Dynamic in size
  - Collection, on the other hand, can hold both homogeneous and heterogeneous elements.
  - Every collection class is implemented based on some standard data structure and hence for every requirement ready-made method support is available.
  - On the other hand, collections can hold only object types data but not the primitive type of data.

**Hierarchy of Collection**   
![Picture2](https://user-images.githubusercontent.com/87074236/193452827-ad034782-5467-4a8b-9449-faecc5cd4016.png)

- **Collection**
  - A framework that provides an architecture to store and manipulate the group of objects.
  - Operations that you perform on data such as searching, sorting, insertion, manipulation, and deletion.
  - Java Collection framework provides many interfaces (Set, List, Queue, Deque) and classes (ArrayList, Vector, LinkedList, PriorityQueue, HashSet, LinkedHashSet, TreeSet).

- **Collection methods**

1. add(obj)
2. addAll(collection obj)
3. remove(obj)
4. removeAll(collection obj)
5. contains(obj)
6. containsAll(collection obj)
7. clear()
8. size()
9. toArray()
10. iterator()
11. isEmpty()

### List 

**Methods**

- add(index, obj) 
- addAll(index, collection)
- remove(index)
- get(index)
- set(index, new)
- indexOf(obj)

**List Interface**
- Use when you want to maintain the order of insertion.
- Use when you want to allow duplicate elements.
- Use index to uniquely identify elements in the list.
- Allows null values.

**ArrayList**
- Implements growable array data structure.
- Allows duplicate elements.
- Preserves the order of insertion.
- Allows heterogeneous elements.
- Allows null insertion.
- Implements Serializable, Cloneable, and Random Access interfaces.
- Initial capacity or ArrayList size is 10.
- Size grows by (current capacity * 3/2) + 1
- suitable when your frequent opertaion is random retrival of elements from list.

**Vector**
- Legacy implementation.
- Vector methods are synchronized and thread-safe.
- Everything else is the same as ArrayList.

**Vector vs ArrayList:**
  - Vector methods are synchronized, and ArrayList's are not.
  - ArrayList is not thread-safe.
  - Vector allows only one thread to perform operations.
  - ArrayList has better performance than Vector.

**LinkedList**
- Implements double linked-list data structure.
- Allows duplicate elements.
- Preserves the order of insertion.
- Allows heterogeneous elements.
- Allows null insertion.
- Implements Serializable and Cloneable, but does not implement RandomAccess.
- Use if you need middle insertion and deletion.
- No initial capacity; it creates on-the-fly as you insert elements.
- Create LinkedList using:
  - Empty constructor
  - Collection constructor
    
![image](https://github.com/codewithheeren/Java/assets/87074236/3901cd51-0649-4f71-acb1-9d07f9e69683)

**Stack**
- LIFO (Last In, First Out).
- Methods:
  - empty: Check if the stack is empty.
  - push: Insert a new element on top of the stack.
  - pop: Retrieve and remove the last element on top of the stack.
  - search: Search for a specific element and return its position.
  - peek: Take a look at the last element on top of the stack without removing it.

Iterate collection 
1. using for each loop
2. using Cursor
    1. Iterator
    2. List Iterator
**Cursors**

Iterator<String> itr = list.iterator();   
while(itr.hasNext()){
    String str = itr.next();
}

**Iterator vs ListIterator**    

-   **Iterator**: Used to traverse elements in forward direction only.
-   Supports basic iteration and removal of elements.
  
-   **ListIterator**: Extends Iterator to allow bidirectional traversal of elements.
-   Supports adding elements, replacing elements and bidirectional iteration.

**Set**   
---

-   Used when duplicate values need not to add to the collection.
-   Also used when sorting is needed in the collection.

**HashSet**  

-   Implements the Hashtable data structure.
-   Represents an unordered collection.
-   Adds elements based on their hashcode.
-   Does not allow duplicates.
-   Allows heterogeneous elements.
-   Allows only one null insertion.
-   Initial capacity is 16, load factor is 0.75 (doubles capacity when 75% full).

**LinkedHashSet**  

-   Child of HashSet.
-   Preserves the order of insertion.
-   Other characteristics are the same as HashSet.

**SortedSet**   

-   Immediate child interface of set interface.

**TreeSet**  

-   Implements a balanced tree data structure.
-   Used for natural or custom sorting (ascending/descending).
-   Default sorting order is ascending.
-   Requires implementation of Comparator for custom sorting.
-   Allows only homogeneous elements.
-   Does not allow null elements.
-   Contains unique elements without duplicates.

**Comparable vs Comparator**

-   Comparable: Used for default sorting.
    -   Contains compareTo() method.
    -   Implemented by all wrapper classes.
-   Comparator: Used for custom sorting.
    -   Contains compare() method.
    -   Implemented when custom sorting is needed.

---------------------------------------------------------------------------
Assignment -

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

