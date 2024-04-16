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
### Useful String Methods
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
### StringBuffer class methods
- append()
- reverse()
- insert()
- charAt()
- substring()
- length()

**Note - Do the implementation on all above methods for better understanding**

### Why string is immutable in java 
![image](https://github.com/codewithheeren/Java/assets/87074236/946e3ecc-2367-483e-99fd-556a1d8325fd)

### Why String is immutable in java 

Following are the reasons - 
- Suppose there are 5 reference variables, all refer to one string object "Ram". If one reference variable changes the value of the object, it will be change for all the reference variables. 
That is why String objects are immutable in Java.
- As the String object is immutable we don't have to take care of the synchronization that is required while sharing an object across multiple threads.

### Why String class is Final in Java?
The reason behind the String class being final is because no one can override the methods of the String class and cant change the immutable behaviour of string class.  

### String Vs String Buffer     

![stringvsstringbuffer](https://github.com/codewithheeren/Java/assets/87074236/ce48dc6d-df4d-4d90-a222-6e6e93201495)

### String Buffer Vs String Builder   

![stringbuffervsstringbuilder](https://github.com/codewithheeren/Java/assets/87074236/f5f68d42-1271-418a-acdd-a2677ffd1ca4)


