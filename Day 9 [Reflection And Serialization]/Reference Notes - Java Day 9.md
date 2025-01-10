## OOPS Day 9

 @author Heeren

 **Topics Covered**
--------------
- Reflection
- Serialization
  - Serialization and Deserialization
  - Serializable
  - Object input stream and object output stream
  - Serialization in inheritance
  - Serialization in association
  - Serialization with static data member
  - Transient keyword
  - Externalizable 
- Enum
- Internal working of Enum
- Design Patterns
	- Singleton Design Pattern  
    	- Breaking and preventing Singleton pattern
    	- Builder design pattern
        - Factory design Pattern
---
## 1. Reflection
<table>
    <tr>
        <td><a href="#">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e4" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">1. Reflection</th>
    </tr>
</table>

🔵 **Reflection** 
Reflection API is use to get metadata, examine and change the run time behavior of a class.
usecase is in  Testing tools , Debugger, IDE etc.

🔵 **How many ways we can create object of a class ?**   
new keyword, reflection , serialization , cloning   

## 2. Serialization
<table>
    <tr>
        <td><a href="#">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e4" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">2. Serialization</th>
    </tr>
</table>

🔵 **What is serialization ?**
Serialization in Java is a process of writing the object state into a byte-stream. It is mainly used in Hibernate, JPA, EJB, etc. technologies.

The reverse operation of serialization is called deserialization where a byte-stream is converted into an object.

The serialization and deserialization process is platform-independent; it means you can serialize an object on one platform and deserialize it on a different platform.

🔵 **Serializable Interface**

- The Serializable interface must be implemented by the class whose object needs to be persisted.

- The String class and all the wrapper classes implement the java.io.Serializable interface by default.

- Serializable is a marker interface.

- If a class implements the Serializable interface, then all its subclasses will also be serializable.

- If a class has a reference to another class, all the references must be Serializable otherwise, the serialization process will not be performed. In such cases, `NotSerializableException` is thrown at runtime.

- If there is any static data member in a class, it will not be serialized because static is part of the class, not the object.
  
🔵 **flush() Method:**
The flush() method is used to clear the internal buffers (if any) and force to write all the pending data into the stream destination.

🔵 **Transient Keyword:**
If you don't want to serialize any data member of a class, you can mark it as transient. For example, marking id as transient will prevent it from being serialized. Consequently, when you deserialize the object after serialization, the value of id will not be restored and will return the default value (0 in the case of an integer).

🔵 **SerialVersionUID:**
- The serialization process at runtime associates an id with each Serializable class which is known as SerialVersionUID. 
- It is used to verify the sender and receiver of the serialized object. The sender and receiver must be the same. To verify it, SerialVersionUID is used.
- The sender and receiver must have the same SerialVersionUID, otherwise,InvalidClassException will be thrown when you deserialize the object. 
- We can also declare our own SerialVersionUID in the Serializable class. To do so, you need to create a field SerialVersionUID and assign a value to it. It must be of the long type with static and final. 
- It is suggested to explicitly declare the serialVersionUID field in the class and have it private also.

```java
import java.io.Serializable;    
class Employee implements Serializable{    
 private static final long serialVersionUID=1L;    
 int id;    
 String name;    
 public Student(int id, String name) {    
  this.id = id;    
  this.name = name;    
 }    
}    
```

🔵 **Externalizable Interface:**    
To have control over reading and writing during serialization and deserialization, we implement the java.io.Externalizable interface. This interface provides methods readExternal() and writeExternal() for customizing serialization behavior. This gives complete control to customize the serialization process, and it can offer relatively fast performance compared to standard serialization.    
  
## 3. Enum
<table>
    <tr>
        <td><a href="#">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e4" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">3. Enum</th>
    </tr>
</table>

- it is use to define constants.
- Enum is use to define user define data type.
- Enum keyword is use to define enum.
- Enum value can only hold in enum type of variable only.
- Enum can use in switch case statement.
- Enum are final so they can not inherit.
- Enum also not extends with any entity in java.
- We can not create enum object , Enum objects implicitly creates.

🔵 **Internal Working**

public enum Day {
	Sun, Mon, Tue, Wed, Thu, Fri, Sat;
}

Internally Enum is nothing but class.
class Day{
	static final Day Sun = new Day();
	static final Day Mon = new Day();
	static final Day Tue = new Day();	
}
Day day = Day.sun;

Enum can also define inside the class and that is known as nested enum.

## 4. Design Patterns 
<table>
    <tr>
        <td><a href="#">
             <img src="https://github.com/user-attachments/assets/393a6073-ba6a-48dd-972b-9e9b8d908e4" alt="yt" width="20" height="20">
        </a></td>
        <th align="left">4. Design Patterns </th>
    </tr>
</table>

🔵 **classification**
- creational Design pattern
- Structural Design Pattern
- Behavioral Design Pattern
  
🔵 **creational Design pattern**  
- Singleton Design Pattern         
	- Breaking and preventing Singleton pattern    
- Builder design pattern    
- Factory design Pattern
- Strategy Pattern   (Behavioral Design Pattern)
