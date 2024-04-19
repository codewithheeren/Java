## OOPS Day 11

 @author Heeren

 **Topics Covered**
--------------
- Map
- Hashmap ,linked hashmap, hashtable,treemap
- Properties
- hashmap internal working
- Contract between equals and hashcode method
- Collection vs concurrent collection
- Concurrent hashmap
- Copy on write array list ,copy on write arrayset
- Difference between concurrent hashmap and hashmap
---

**Hierarchy of Map**     
![Picture1](https://user-images.githubusercontent.com/87074236/193452840-96d05ebf-ff3b-471c-aa16-e48514b20a91.png)    

## Map

- Store data in the form of key-value pairs.
- Keys cannot be duplicate (unique), but values can be.
- Each entry in the map is represented by the `Map.Entry` interface.
  
  Example:
  ```java
  Map.Entry entry;
  entry.getKey();
  entry.getValue();
  entry.setValue();
### Map Methods

-   `put(key, value)`
-   `putAll(mapObj)`
-   `get(key)`
-   `remove(key)`
-   `containsKey(key)`
-   `containsValue(value)`
-   `keySet()`
-   `values()`
-   `clear()`
-   `size()`
-   `entrySet()`
-   `isEmpty()`

### HashMap

-   Implements hashtable data structure.
-   Adds new elements based on the hash code of the key object.
-   Contains only unique keys.
-   Allows one null key and multiple null values.
-   Initial default capacity is 16 with a load factor of 0.75.

### TreeMap

-   Implements red-black tree data structure.
-   Supports custom sorting of keys.
-   Homogeneous elements.

### Internal Working of HashMap

-   HashMap contains an array of nodes.
-   Hash code of the key determines the bucket index.
-   Each bucket is a linked list of nodes, where each node contains hash code, key, value, and a reference to the next node.

### HashMap vs Hashtable

| Feature | HashMap | Hashtable |
| --- | --- | --- |
| Synchronization | Not synchronized | Synchronized |
| Null Values | Allows one null key and multiple null values | Does not allow null keys or values |
| Performance | Faster | Slower |
| Iterator | Fail-fast (throws ConcurrentModificationException) | Fail-safe (operates on a clone of the collection) |

### Properties

-   Extends the `Hashtable` class to manage key-value pairs.

-   Commonly used for storing configuration data.    

```java
Properties properties = new Properties();

try (FileInputStream fis = new FileInputStream("config.properties")) {

    properties.load(fis);

}

String value = properties.getProperty("key");

properties.setProperty("newKey", "newValue");

properties.remove("keyToRemove");

int size = properties.size();

properties.clear();
```
markdownCopy code

`## Map

- Store data in the form of key-value pairs.
- Keys cannot be duplicate (unique), but values can be.
- Each entry in the map is represented by the `Map.Entry` interface.

  Example:
  ```java
  Map.Entry entry;
  entry.getKey();
  entry.getValue();
  entry.setValue(); `

### Map Methods

-   `put(key, value)`
-   `putAll(mapObj)`
-   `get(key)`
-   `remove(key)`
-   `containsKey(key)`
-   `containsValue(value)`
-   `keySet()`
-   `values()`
-   `clear()`
-   `size()`
-   `entrySet()`
-   `isEmpty()`

### HashMap

-   Implements hashtable data structure.
-   Adds new elements based on the hash code of the key object.
-   Contains only unique keys.
-   Allows one null key and multiple null values.
-   Initial default capacity is 16 with a load factor of 0.75.

### TreeMap

-   Implements red-black tree data structure.
-   Supports custom sorting of keys.
-   Homogeneous elements.

### Internal Working of HashMap

-   HashMap contains an array of nodes.
-   Hash code of the key determines the bucket index.
-   Each bucket is a linked list of nodes, where each node contains hash code, key, value, and a reference to the next node.

### HashMap vs Hashtable

| Feature | HashMap | Hashtable |
| --- | --- | --- |
| Synchronization | Not synchronized | Synchronized |
| Null Values | Allows one null key and multiple null values | Does not allow null keys or values |
| Performance | Faster | Slower |
| Iterator | Fail-fast (throws ConcurrentModificationException) | Fail-safe (operates on a clone of the collection) |

### Properties

-   Extends the `Hashtable` class to manage key-value pairs.

-   Commonly used for storing configuration data.

    Example:

    javaCopy code

    `Properties properties = new Properties();
    try (FileInputStream fis = new FileInputStream("config.properties")) {
        properties.load(fis);
    }

    String value = properties.getProperty("key");
    properties.setProperty("newKey", "newValue");
    properties.remove("keyToRemove");
    int size = properties.size();
    properties.clear();`

### Concurrent Collections

-   `ConcurrentHashMap`
-   `CopyOnWriteArrayList`
-   `CopyOnWriteArraySet`

### Fail-Fast Iterator vs Fail-Safe Iterator

-   Fail-Fast Iterator:
    -   Throws `ConcurrentModificationException` if the collection is modified during iteration.
-   Fail-Safe Iterator:
    -   Operates on a snapshot or cloned version of the collection.
    -   Does not throw exceptions if the underlying collection is modified during iteration.Example:

```java
List<String> list = new ArrayList<>();
list.add("A");
list.add("B");
Iterator<String> iterator = list.iterator();
while (iterator.hasNext()) {
    System.out.println(iterator.next());
    list.add("C"); // Throws ConcurrentModificationException
}

List<String> list = new CopyOnWriteArrayList<>();
list.add("A");
list.add("B");
Iterator<String> iterator = list.iterator();
while (iterator.hasNext()) {
    System.out.println(iterator.next());
    list.add("C"); // No exception; operates on a snapshot
}

```
