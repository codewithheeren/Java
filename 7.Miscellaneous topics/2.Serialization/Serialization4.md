## Java Serialization with Aggregation

```java
/**
 * If a class has a reference to another class, all the references must be Serializable otherwise serialization process will not be performed.
 * In that case you will get NotSerializableException  
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.Serialization;

import java.io.FileInputStream;
import java.io.FileOutputStream;
import java.io.ObjectInputStream;
import java.io.ObjectOutputStream;
import java.io.Serializable;

class Address{    
 String addressLine,city,state;    
 public Address(String addressLine, String city, String state) {    
  this.addressLine=addressLine;    
  this.city=city;    
  this.state=state;    
 }    
}    

import java.io.Serializable;  
public class Student implements Serializable{  
 int id;  
 String name;  
 Address address;//HAS-A  
 public Student(int id, String name) {  
  this.id = id;  
  this.name = name;  
 }  
}  

```
---