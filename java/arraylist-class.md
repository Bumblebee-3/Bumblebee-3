# `java.util.ArrayList` Class
The `ArrayList` class is present in the `java.util` package
```java
import java.util.ArrayList;
```

It is similar to an array. It stores elements of a single type.
However, it is resizeable. You can change the length of the ArrayList.

**NOTE:** You cannot use primitive data types, use the corresponding wrapper class instead.

## Initialisation
Object of the `ArrayList` class are parameterized (explained in detail later), i.e. it requires the type of the class whose objects will be stored.
```java
ArrayList<String> arrayList = new ArrayList<String>(); 
```

Notice the `<>` after the class name. This is the parameter, which shows that objects of the `String` class will be stored in the `ArrayList`
You can remove the parameter (leaving behind only `()`) from the initialization, but not the declaration.

```java
ArrayList<String> arrayList = new ArrayList<>(); 
```

In functions, the formal arguments require the parameterized types, and the actual arguments don't
```java
public static void function(ArrayList<String> arrayList) {
  function(new ArrayList<>()); // This code has no purpose and is just an example
}
```

## Important Methods
**NOTE:** The type `T` used refers to the parameterized type.
| Method | Descripion |
|---|---|
| `add(T element)` | Adds the element `element` to the end of the list |
| `add(int index, T element)` | Adds the element `element` at index `index` <br><br> Eg. For an `ArrayList<Integer>` <br> {1,2,3} -> `add(1,3)` -> {1,1,2,3} |
| `clear()` | Clears the list (removes all elements) |
| `contains(T element)` | Returns `true` if `element` is in the list, else `false` |
| `get(int index)` | Equivalent to `arr[index]` for index |
| `indexOf(T element)` | Returns the index of the first occurrence of `element` or -1 if not present |
| `lastIndexOf(T element)` | Returns the index of the last occurrence of `element` or -1 if not present |
| `remove(int index)` | Removes the element at `index` and shifts all the indices greater than `index` to the previous index (9 to 8, 8 to 7, ...). Returns the removed element |
| `remove(T element)` | Removes the first occurence of `element` if present. Returns whether element was present |
| `set(int index, T element)` | Sets element at `index` to `element` |
| `size()` | Returns the number of elements in the list |
| `toArray()` | Converts the list to a fixed-size array. Returns the array `T[]`. |

## Array <-> ArrayList
 - Array to ArrayList: 
```java
import java.util.Arrays;

...

  ArrayList<type> list = Arrays.asList(array); // Substitute type as the type of the array
```

- ArrayList to Array

```java
type[] array = list.toArray();
```
