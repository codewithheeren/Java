## OOPS Day 7

 @author Heeren

**Topics Covered**
--------------
1. [What is String in Java?](#1-what-is-string-in-java)
   - String literal and string object
   - String comparison 
   - Plus Operator and concat method
   - Why string not prefer to store secure information like password
   - Useful Methods of string class
2. [Why String is Immutable and Final in Java?](#2-why-string-is-immutable-and-final-in-java)
3. [Differences between String and String Buffer and String builder](#3-differences-between-string-and-string-buffer-and-string-builder)
   - String buffer 
   - String builder
   - Difference between string and string buffer
   - Difference between string buffer and string builder
4. [Assignment](#4-assignment)    
--------------

## 1. What is String in java?
<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instanceof-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">String in java</th>
    </tr>
</table>

🔵 **How many ways string can be represent in java ?**    
🔵 **what are the different wrapper classes use to represent string in java ?**    
🔵 **Useful Methods of string class**     
- equals
- equalIgnoreCase
- valueOf
- toCharArray
- concat
- toUpperCase
- toLowerCase
- charAt   
- length
- indexOf
- subString
- replaceAll
- split(" ")
- trim
- isEmpty
  
🔵 **StringBuffer class methods**
- append()
- reverse()
- insert()
- charAt()
- substring()
- length()

**Note - Do the implementation on all above methods for better understanding**

## 2. Why string is immutable and final in java? 
<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instanceof-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">Why string is immutable and final</th>
    </tr>
</table>

![image](https://github.com/codewithheeren/Java/assets/87074236/946e3ecc-2367-483e-99fd-556a1d8325fd)

Following are the reasons -    
🔵 Suppose there are 5 reference variables, all refer to one string object "Ram". If one reference variable changes the value of the object, it will be change for all the reference variables.    
That is why String objects are immutable in Java.     
🔵 As the String object is immutable we don't have to take care of the synchronization that is required while sharing an object across multiple threads.    

🔵 **Why String class is Final in Java?**     
The reason behind the String class being final is because no one can override the methods of the String class and cant change the immutable behaviour of string class.  

## 3. Differences between String and String Buffer and String builder     
<table>
    <tr>
        <td><a href="https://youtu.be/link-to-instanceof-video">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e45" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">String Vs String Buffer Vs String builder</th>
    </tr>
</table>

🔵 **String Vs String Buffer**     
![stringvsstringbuffer](https://github.com/codewithheeren/Java/assets/87074236/ce48dc6d-df4d-4d90-a222-6e6e93201495)

🔵 **String Buffer Vs String Builder**    

![stringbuffervsstringbuilder](https://github.com/codewithheeren/Java/assets/87074236/f5f68d42-1271-418a-acdd-a2677ffd1ca4)

## 4. Assignment    

### Problem 1: Reverse a String
Write a function that takes a string as input and returns the reverse of that string.

**Input:** "hello"
**Output:** "olleh"

### Problem 2: Count the Occurrences of a Character
Write a function that takes a string and returns the number of occurrences of each character in the string.

**Input:** "hello"
**Output:** h - 1 times, e - 1 times, l - 2 times, o - 1 times

### Problem 3: Check if a String is a Palindrome
Write a function that takes a string as input and returns True if it is a palindrome (reads the same forwards and backwards), and otherwise returns False.

**Input:** "radar"
**Output:** Entered string is palindrome.

**Input:** "hello"
**Output:** Entered string is not a palindrome.

### Problem 4: Remove Duplicates from a String
Write a function that takes a string as input and removes all the duplicate characters, returning the modified string.

**Input:** "aabbcdd"
**Output:** "abcd"

### Problem 5: Capitalize the First Letter of Each Word in a Sentence
Write a function that takes a sentence as input and capitalizes the first letter of each word.

**Input:** "this is a sample sentence"
**Output:** "This Is A Sample Sentence"

### Problem 6: Count the Occurrences of a Specific Character in a String
Write a function that takes a string and a character as input and returns the number of occurrences of that character in the string.

**Input:** "hello world" and a character (e.g., "o")
**Output:** 'o' occurred 2 times in the entered string.

### Problem 7: Check if Two Strings are Anagrams
Write a function that takes two strings as input and returns True if they are anagrams of each other, and False otherwise.

**Input:** "listen" and "silent"
**Output:** Entered strings are anagrams.

**Input:** "hello" and "world"
**Output:** Entered strings are not anagrams.

### Problem 8: Remove All Whitespace Characters from a String
Write a function that takes a string as input and removes all the whitespace characters, returning the modified string.

**Input:** "hello world"
**Output:** "helloworld"

### Problem 9: Find the Longest Common Prefix Among a Group of Strings
Write a function that takes a list of strings as input and returns the longest common prefix among them.

**Input:** ["apple", "appetite", "apprehend"]
**Output:** The longest common prefix - "app"

### Problem 10: Convert a String to Uppercase or Lowercase
Write a function that takes a string and a flag indicating uppercase or lowercase conversion, and returns the modified string.

**Input:** A string, e.g., "Hello", and a flag indicating lowercase
**Output:** Modified string in lowercase, e.g., "hello"

### Problem 11: Swapping Two Strings Without Using a Third Variable
Write a function that takes two strings as input and swaps their values without using a third variable.

**Input:** "hello" and "world"
**Output:** Strings swapped, so the first string becomes "world" and the second string becomes "hello".

### Problem 12: Check if a String is a Rotation of Another String
Write a function that takes two strings as input and returns True if one string is a rotation of the other string, and False otherwise.

**Input:** "apple" and "leapp"
**Output:** True (since "leapp" is a rotation of "apple")

**Input:** "hello" and "world"
**Output:** False (since "world" is not a rotation of "hello")

### Problem 13: Reverse Each Word of a String in a Sentence
Write a function that takes a sentence as input and reverses each word in the sentence.

**Input:** "hello world"
**Output:** "olleh dlrow"

### Problem 14: Print the First Non-Repeated Character in a String
Write a function that takes a string as input and prints the first non-repeated character in the string.

**Input:** A string, e.g., "hello"
**Output:** The first non-repeated character, e.g., "h"

### Problem 15: Print All Duplicate Characters in a String
Write a function that takes a string as input and prints all the duplicate characters present in the string.

**Input:** "programming"
**Output:** r, g, m

### Problem 16: Print the Largest Word in a String Sentence
Write a function that takes a sentence as input and prints the largest word in the sentence.

**Input:** "This is a sample sentence"
**Output:** The largest word - "sentence"

### Problem 17: Reverse a String Without Using a Third Variable
Write a function that takes a string as input and returns the reverse of that string without using a third variable.

**Input:** "hello"
**Output:** "olleh"



