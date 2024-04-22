## Enum

```java
/**
 * Role of Enum in switch case
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.enum;
public enum Day {
	Sun, Mon, Tue, Wed, Thu, Fri, Sat
}

package com.codewithheeren.enum;
public class AccessEnum {      
    public static void main(String args[])    
    {    
      Day[] DayNow = Day.values();    
        for (Day day : DayNow)    
        {    
             switch (day)    
             {    
                 case Sun:    
                     System.out.println("Sunday");    
                     break;    
                 case Mon:    
                     System.out.println("Monday");    
                     break;    
                 case Tue:    
                     System.out.println("Tuesday");    
                     break;         
                 case Wed:    
                     System.out.println("Wednesday");    
                     break;    
                 case Thu:    
                     System.out.println("Thursday");    
                     break;    
                 case Fri:    
                     System.out.println("Friday");    
                     break;    
                 case Sat:    
                     System.out.println("Saturday");    
                     break;    
             }    
         }    
     }    
}   
```
---
