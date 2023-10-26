
**Assignment**

**1.list of string - add elements , use iterator to print and remove elements.**

**2.list of string - add elements , use List iterator iterate in backward direction and print elements.**

**3. Use for each loop to iterate collection and print value of the collection.**

**4. Add integer values in tree set and using comparator sort them in descending order.**




—---------------------------------------------------------------------------------

**Collection** 

**Immutable class** 

Class must be final.

All data members of the class must be final.

All data members must be private.

All data members must be initialized by constructor .

Class should only contain  getter methods. No setter allow.

- Array vs Collection
  - Array
    - Fix in size
    - Arrays can hold the only the same type of data in its collection i.e only homogeneous data types elements are allowed in case of arrays.
    - Do not implement any data structure
    - Arrays can hold both object and primitive type data.
  - Collection
    - Dynamic in size
    - Collection, on the other hand, can hold both homogeneous and heterogeneous elements.
    - Every collection class is implemented based on some standard data structure and hence for every requirement ready-made method support is available being a performance.
    - On the other hand, collection can hold only object types but not the primitive type of data.

**Hierarchy of Collection**

- ![](Aspose.Words.91da75bd-c2a8-4d29-9a20-3db779683afe.001.png)

![](Aspose.Words.91da75bd-c2a8-4d29-9a20-3db779683afe.002.png)

- Collection
  - a framework that provides an architecture to store and manipulate the group of objects.
  - operations that you perform on a data such as searching, sorting, insertion, manipulation, and deletion.
  - Java Collection framework provides many interfaces (Set, List, Queue, Deque) and classes (ArrayList, Vector, LinkedList, PriorityQueue, HashSet, LinkedHashSet, TreeSet).
  - Collection methods
    - add(obj)
    - addAll(collection obj)
    - remove(obj)
    - removeAll(collection obj)
    - contains(obj)
    - containsAll(collection obj)
    - clear
    - size
    - toArray
    - iterator()
    - isEmpty


- List 🡪 interface
  - Use when want to maintain order of insertion
  - Use when want duplicate
  - Use index to uniquely identify element in the list
  - Allow null value
  - List methods:
    - add(index, obj)
    - addAll(index, collection)
    - remove(index)
    - get(index)
    - set(index, new)
    - indexOf(obj)
- ArrayList
  - Implemental growable array data structure
  - Allows duplicate elements 
  - order of insertion is preserves
  - allow heterogeneous elements
  - allow null insertion
  - implements serializable, cloneable, and random-access interface
    - serializable
    - cloneable
      - make copy of the arraylist
    - random access 	// if want to have random retrieve, use arraylist
      - random access arraylist elements
  - initial capacity or arraylist size is 10
  - size grow by (current capacity \* 3/2) + 1
  - create the arraylist by empty constructor and pass in collection constructor
    - new ArrayList(55)
    - new ArrayList(set);
- Vector
  - Vector is legacy
  - Vector methods is synchronized, thread safe	// use if want sync and thread safe
  - Everything else is the same as arraylist 
  - Vector vs arraylist
    - Vector methods is synchronize and arraylist is not
    - Arraylist is not thread safe
    - Vector allow only one thread to perform operation
    - Arraylist better performance than vector
- LinkedList
  - Implement double linkedlist data structure
  - Allows duplicate elements 
  - order of insertion is preserves
  - allow heterogeneous elements
  - allow null insertion
  - implements serializable, cloneable, and do not implement random-access
  - use if need middle insertion and deletion
  - no initial capacity, create on the fly as you insert element
  - create linkedlist by empty constructor and pass in collection constructor
- Stack
  - Lifo 🡪 last in first out
  - Have methods:
    - Empty
      - Check if stack is empty
    - Push
      - Insert new element on the top of stack
    - pop
      - Retrieve last element  on top of stack and that element
    - Search 
      - Search for the specific element and return the position of it
    - Peek 
      - Take a look of the last element on top of the stack without removing it
- Set 🡪 interface
  - An unordered collection or list in which duplicates are not allowed
  - allow heterogeneous elements
  - Perform sorting
  - Set don’t have methods
- HashSet
  - Implement Hashtable data structure
  - Unordered collection
  - Add element base on the hashcode on the element
  - Duplicates are not allowed, if try to add duplicate elelement, code still work, just the element won’t be added
  - allow heterogeneous elements
  - allow only one null insertion
  - hashset initial capacity is 16, load factor is .75 meaning when capacity size reach 75%, then size increase, increase size by double
- Linked HashSet
  - Child of hashset
  - Order of insertion preserve
  - Everything else is the same as hashset
- SortedSet 🡪 interface
  - Add element in sorting order, ascending or descending order
  - If want natural sorting or custom sorting
  - doesn’t retain the insertion order
- TreeSet
  - Implement data structure balance tree
  - Element added in ascending sorting order
  - If want custom sorting, need to pass comparable object
  - Allow homogeneous element only
  - Implement serializable and cloneable interface
  - Do not allow null element
  - contains unique elements, no duplicate
- Cursors
  - Enumeration
    - Can only read data of collection
    - Using for each loop to read data collection
  - Iterator
    - Get element one by one from collection and perform operation such as read and remove
    - Cannot add element
    - Can be use for any collection
    - Loop through in forward direction only
    - Iterator itr = list.iterator();
    - While (its.hasNext(){
      - ` `String str = (String)itr.next();
    - }
  - List Iterator
    - hasNext and next method for forward direction
    - hasPrevious and previous method for reverse direction
    - support add, remove, update, read
    - It is not applicable for all collection API.
    - Parallel iteration of elements is not supported by list Iterator.

**	

**Contract between equals and hashcode methods**

If two objects are equal according to the equals(Object) method, then calling the hashcode() method on each of the two objects must produce the same integer result.


Today’s Mock topics :

1. What is process and what is thread and their differences?
1. what is multithreading?
1. What is the advantage of multithreading ?
1. How many ways we can create thread ?
1. Which approach is better ?
1. Can we run same thread twice ?
1. What is thread priority?
1. What is Thread Life Cycle ?
1. What is the use of Join method ?
1. What is the use of yield method ?
1. What is the use of sleep method?
1. What is dead lock ?
1. What is thread scheduler in java ?
1. What is the difference between start() and run() method call ?
1. Can we overload run method ?
1. What will happen if we don’t override the Thread class run() method?
1. Can  we override start method of thread class ?
1. What happen when we call run method explicitly?
1. What is  the purpose of wait,notify and notify all?
1. What is inter thread communication ? 
1. What Synchronization and what is the advantage and disadvantage of synchronization?
1. Synchronized block vs synchronized method ?
1. What is daemon thread ?
1. What is the difference notify and notify all ?


**Collection Framework** 


||
| :- |
||
||
||
||
||
||
||
||
||
||
||


