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
//1.remove vovel from string - Hello and print.
	//part 2 //get String as an output
	/*
	String s="Hello";
	Stream<Character> stream = s.chars().mapToObj(c->(char)c);
	stream.filter(c -> c != 'e').filter(c -> c != 'o').forEach(System.out::print);
	//2
	s=s.chars().mapToObj(c->(char)c)
	.filter(c->(!(c=='a'||c=='e'||c=='i'||c =='o'))).
	map(String::valueOf).collect(Collectors.joining());
	
	*/
	
	//2.Filter all values greater than 2 in an array,then multiply each value by 3,then sum the values
	//part 2 //do that without using sum method.
	/*
	 int x = Arrays.stream(new int[]{1,2,3,4,5,6,7,8,9}).filter(i->i>2).map(i->i*3).sum();
	 System.out.println(x);
	 //2
	 int x = Arrays.stream(new int[] {2,3,4,5,6,7}).filter(a -> a>2).reduce(0,((c,v)-> c+v));
	 System.out.println(x);	
	*/
	
	//3.convert all strings with length greater than 3 into uppercase strings,then sort alphabetically
	//part 2 // get String[] as output.
	/*
	Arrays.stream(new String[] {"Bus", "car", "bicycle", "train"}).filter(s->s.length()>3)
	.map(String::toUpperCase).sorted().forEach(System.out::println);
	
	//	String[] array =Arrays.asList("Hello","hi","bye","will meet tomorrow").stream().
	 	 filter(s->s.length()>3).map(String::toUpperCase).sorted().toArray(String[]::new);
		System.out.println(Arrays.toString(array));
	
	*/
	
	//4.filter only the first 3 strings in {"Bus", "car", "bicycle", "train"}
	/*
	Stream.of("Bus", "car", "bicycle", "train").limit(3).forEach(System.out::println);
	*/
	
	//5.Remove all duplicate values in a list of numbers  without converting into a set 
	
	/*
	Arrays.stream(new int[]{1,2,3,4,4,4,3,2,8,9}).distinct().forEach(System.out::println);
	*/
	
	//6.{"Bus", "car", "bicycle", "train"}
	//Stream.of("Hello").map(s->new StringBuilder(s).reverse()).forEach(System.out::println);
	
	//reverse array using stream
	
	//convert array in to reverse order.
	Integer[] array = Arrays.stream(new Integer[]{1,2,3,4,5,6}).sorted((Comparator<Integer>)(x,y) -> -1)
	.toArray(Integer[] :: new);
	//System.out.println(Arrays.toString(array));
	
	
	//remove all the spaces from string
	String s = "hello hi bye how are you";
	s = Stream.of(s).map(a -> a.replaceAll(" ", "")).collect(Collectors.joining());
	//System.out.println(s);
	}
}
```
---
