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
- Stack
- Set
- Hashset
- linkedhashset
- Sortedset
- Treeset
- iterator
- List iterator
- Comparable vs comparator
- Map
- Hashmap ,linked hashmap, hashtable,treemap
- Properties
- hashmap internal working
- Contract between equals and hashcode method
- collection vs concurrent collection
- Concurrent hashmap
- copy on write array list ,copy on write arrayset
- difference between concurrent hashmap and hashmap
- diffence between arraylist and list 
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

![Picture1](https://user-images.githubusercontent.com/87074236/193452840-96d05ebf-ff3b-471c-aa16-e48514b20a91.png)

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

**ArrayList**
- implements growable array data structure
- ArrayList capacity: **(Current capacity * 3/2) + 1**
- Creating a new ArrayList: **List<String> list = new ArrayList<>();**

**Cursors**

Iterator<String> itr = list.iterator();   
while(itr.hasNext()){
    String str = itr.next();
}
