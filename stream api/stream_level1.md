## Stream conversions

### StreamBasics.java

```java
/**
 * This class implements stream api level 1.
 * @author Heeren
 * @version 1.0
 */
 import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
import java.util.Set;
import java.util.function.Function;
import java.util.stream.Collectors;
import java.util.stream.Stream;

public class StreamBasics1 {
public static void main(String[] args) {
//1	
	Arrays.asList(2,3,1,4,5,3).stream();
//2
	int[] array = {1,2,3,4,5,6};
	Arrays.stream(array);        
//3
	String string = "Hello";
	Stream<Character> stream = string.chars().mapToObj(s->(char)s);
	stream.filter(c->(c != 'e')||(c != 'o')).forEach(System.out::println);
			//collect(Collectors.joining());
	//System.out.println(s);
	
//4
	Stream.of(1,2,3,4,5,6,7);
	
	//Terminal Operations
	//1
	List<Integer> list = Stream.of(1,2,3,4,5,6,7).collect(Collectors.toList());
	//System.out.println(list);
	
	//2
	Set<Integer> set = Stream.of(1,2,3,4,5,3,6,7).collect(Collectors.toSet());
//	System.out.println(set);
	
	//3
	List<Integer> arrayList = Stream.of(1,2,3,4,5,3,6,7).collect(Collectors.toCollection(ArrayList::new));
//	System.out.println(arrayList);
	
	//4
	Integer[] a = Stream.of(1,2,3,4,5,3,6,7).toArray(Integer[]::new);
//	System.out.println(Arrays.toString(a));
	
	//5
	String s1 = Stream.of("Hello","Hi","Bye").collect(Collectors.joining());
	//System.out.println(s1);
	
	String s2 = Stream.of(1,2,3,4,5).map(String::valueOf).collect(Collectors.joining());
//	System.out.println(s2);
	
	//convert into map
	Arrays.asList(new Employee(1, "A", 15000), new Employee(2, "A", 20000), new Employee(3, "B", 30000),
	new Employee(4, "B", 40000), new Employee(5, "C", 50000), new Employee(6, "C", 60000)).stream().
	collect(Collectors.toMap(Employee::getId, Function.identity())).entrySet()
	.forEach(System.out::println);
	
	//convert into map
	Arrays.asList(new Employee(1, "A", 15000), new Employee(2, "A", 20000), new Employee(3, "B", 30000),
			new Employee(7, "B", 40000), new Employee(5, "C", 50000), new Employee(6, "C", 60000)).stream().
			collect(Collectors.toMap(e->e.getId(), Function.identity())).entrySet()
			.forEach(System.out::println);
	
	
//intermediate methods
//	count
//	max
//	min
//	limit(2)
//	disctinct 
}
}
```
