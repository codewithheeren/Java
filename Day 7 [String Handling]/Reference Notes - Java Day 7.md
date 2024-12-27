## OOPS Day 7

 @author Heeren

 **Topics Covered**
--------------
### String Handling
- String
- String literal and string object
- Immutability of String 
- String buffer 
- String builder
- Difference between string and string buffer
- Difference between string buffer and string builder
- Methods of string 
- String comparison 
- Plus Operator and concat method
- Why string not prefer to store secure information like password
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

## 2. Why string is immutable and final in java ? 
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


