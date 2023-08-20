## Array Basics - 

### Declaration of arrays - 
```java
		int[] array1 = new int[5];
		array1[0] = 10;
		array1[1] = 20;
		array1[2] = 30;
		System.out.println(Arrays.toString(array1));

		int[] array2 = { 100, 200, 300, 400 };
		System.out.println(Arrays.toString(array2));

		int[] array3 = new int[] { 100, 200, 300, 400 };
		System.out.println(Arrays.toString(array3));
```
---		
### Arrays Utility Class Useful Methods
```java
int[] array = {1, 2, 3, 4, 5};
String arrayAsString = Arrays.toString(array);
output arrayAsString: "[1, 2, 3, 4, 5]"
asList - Convert array to list collection.
```
---	
 ```java
Integer[] array = {10, 20, 30, 40, 50};
List<Integer> list = Arrays.asList(array);
output list: [10, 20, 30, 40, 50]
stream().forEach
```
---	
```java
List<Integer> list = Arrays.asList(1, 2, 3, 4, 5);
list.stream().forEach(System.out::println);
Output:
1
2
3
4
5

```
---	
```java
int[] array = {5, 3, 1, 4, 2};
Arrays.sort(array);
output array: [1, 2, 3, 4, 5]
```
---	
```java
int[] array = {1, 2, 3, 4, 5};
int index = Arrays.binarySearch(array, 3);
output index: 2
```
---	
```java
int[] array = new int[5];
Arrays.fill(array, 10);
output array: [10, 10, 10, 10, 10]
```
---	
```java
int[] originalArray = {1, 2, 3};
int[] newArray = Arrays.copyOf(originalArray, 5);
output newArray: [1, 2, 3, 0, 0]
```
---	
```java
int[] array1 = {1, 2, 3};
int[] array2 = {1, 2, 3};
boolean areEqual = Arrays.equals(array1, array2);
output areEqual: true
```
---	
```java
int[] array = new int[5];
Arrays.fill(array, 10);
output array: [10, 10, 10, 10, 10]
```
---	

## Array Manipulation Problems

### Problem 1: Java Program to Find the Frequency of Each Element in an Array
Write a Java program that takes an array as input and prints the frequency of each element in the array.

**Input:** An array, e.g., [1, 2, 2, 3, 1, 4, 5]
**Output:** Element 1 occurs 2 times, Element 2 occurs 2 times, Element 3 occurs 1 time, Element 4 occurs 1 time, Element 5 occurs 1 time

### Problem 3: Java Program to Print the Elements of an Array in Reverse Order
Write a Java program that takes an array as input and prints its elements in reverse order.

**Input:** An array, e.g., [3, 7, 1, 9, 5]
**Output:** 5, 9, 1, 7, 3

### Problem 4: Java Program to Print the Elements of an Array Present on Even Positions
Write a Java program that takes an array as input and prints the elements of the array present on even positions.

**Input:** An array, e.g., [3, 7, 1, 9, 5]
**Output:** 7, 9

### Problem 6: Java Program to Print the Largest Element in an Array
Write a Java program that takes an array as input and prints the largest element in the array.

**Input:** An array, e.g., [3, 7, 1, 9, 5]
**Output:** The largest element is 9

### Problem 7: Java Program to Print the Smallest Element in an Array
Write a Java program that takes an array as input and prints the smallest element in the array.

**Input:** An array, e.g., [3, 7, 1, 9, 5]
**Output:** The smallest element is 1

### Problem 8: Java Program to Print the Number of Elements Present in an Array
Write a Java program that takes an array as input and prints the number of elements present in the array.

**Input:** An array, e.g., [3, 7, 1, 9, 5]
**Output:** The number of elements is 5

### Problem 9: Java Program to Print the Sum of All the Items of the Array
Write a Java program that takes an array as input and prints the sum of all the items in the array.

**Input:** An array, e.g., [3, 7, 1, 9, 5]
**Output:** The sum of all items is 25

### Problem 10: Java Program to Copy All Elements of One Array into Another Array
Write a Java program that takes two arrays as input and copies all elements of the first array into the second array.

**Input:** Two arrays, e.g., [3, 7, 1, 9, 5] and [0, 0, 0, 0, 0]
**Output:** The second array after copying: [3, 7, 1, 9, 5]

### Problem 11: Linear Search
Write a Java program that takes an array and a target element as input and performs linear search to find the index of the target element.

**Input:** An array, e.g., [3, 7, 1, 9, 5], and target element 7
**Output:** The index of 7 is 1

### Problem 12: Binary Search
Write a Java program that takes a sorted array and a target element as input and performs binary search to find the index of the target element.

**Input:** A sorted array, e.g., [1, 3, 5, 7, 9], and target element 5
**Output:** The index of 5 is 2

### Problem 13: Selection Sorting
Write a Java program that takes an array as input and performs selection sorting on its elements.

**Input:** An array, e.g., [3, 7, 1, 9, 5]
**Output:** The sorted array: [1, 3, 5, 7, 9]

### Problem 14: Bubble Sorting
Write a Java program that takes an array as input and performs bubble sorting on its elements.

**Input:** An array, e.g., [3, 7, 1, 9, 5]
**Output:** The sorted array: [1, 3, 5, 7, 9]

### Problem 15: Find Missing Number in the Array
Write a Java program that takes an array as input and finds the missing number in the sequence.

**Input:** An array, e.g., [1, 2, 3, 4, 6, 7, 8, 9]
**Output:** The missing number is 5

### Problem 16: Find Second Largest Number in an Array
Write a Java program that takes an array as input and finds the second largest number.

**Input:** An array, e.g., [3, 7, 1, 9, 5]
**Output:** The second largest number is 7

### Problem 17: Separate Odd and Even Numbers in an Array
Write a Java program that takes an array as input and separates odd and even numbers.

**Input:** An array, e.g., [1, 2, 3, 4, 5, 6, 7, 8, 9]
**Output:** Odd numbers: [1, 3, 5, 7, 9], Even numbers: [2, 4, 6, 8]

### Problem 18: Find Peak Element in the Array
Write a Java program that takes an array as input and finds the peak element.

**Input:** An array, e.g., [1, 3, 5, 2, 4, 6, 8]
**Output:** The peak element is 5

### Problem 19: Find the Maximum Difference Between Two Elements in an Array
Write a Java program that takes an array as input and finds the maximum difference between two elements.

**Input:** An array, e.g., [4, 2, 10, 8, 7]
**Output:** The maximum difference is 8

### Problem 20: Find the kth Smallest Element in an Array
Write a Java program that takes an array and an integer k as input and finds the kth smallest element.

**Input:** An array, e.g., [4, 2, 10, 8, 7], and k = 3
**Output:** The 3rd smallest element is 7

### Problem 21: Remove Duplicates from an Array
Write a Java program that takes an array as input and removes duplicates.

**Input:** An array, e.g., [3, 2, 5, 2, 8, 5]
**Output:** The array after removing duplicates: [3, 2, 5, 8]

### Problem 22: Find the Intersection of Two Arrays
Write a Java program that takes two arrays as input and finds their intersection.

**Input:** Two arrays, e.g., [3, 2, 5, 8], and [5, 2, 9]
**Output:** The intersection of arrays: [2, 5]

### Problem 23: Find the Union of Two Arrays
Write a Java program that takes two arrays as input and finds their union.

**Input:** Two arrays, e.g., [3, 2, 5, 8], and [5, 7, 9]
**Output:** The union of arrays: [3, 2, 5, 8, 7, 9]

### Problem 24: Find the Subarray with the Maximum Sum
Write a Java program that takes an array as input and finds the subarray with the maximum sum.

**Input:** An array, e.g., [-2, 1, -3, 4, -1, 2, 1, -5, 4]
**Output:** The subarray with the maximum sum: [4, -1, 2, 1]
