## Enum

```java
/**
 * Parameterize constructor in enum
 * @author Heeren
 * @version 1.0
 */
package com.codewithheeren.enum;
enum Season {
	WINTER(5), SPRING(10), SUMMER(15), FALL(20);
	int temprature;
	private Season(int temprature) {
		this.temprature = temprature;
	}
}

package com.codewithheeren.enum;
class EnumExample4 {
	public static void main(String args[]) {
	Season[] seasons = Season.values();
	for (Season season :seasons){
	System.out.println(season + " temprature :" + season.temprature);
    }	
  }
}
```
---
