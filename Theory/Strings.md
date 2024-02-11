```java

String name = "Kumar Manglam"
```

### How does it work internally and its memory management?

Most commonly used. It is a Class. Every string we create is a object of type String.

String             name = "Kumar Manglam"
    |                     |                       |
Datatype     ref-variable         object

```java
String a = "Kumar";
String b = "Kumar";
Question - wether a and b is pointing to same object or different?
Answer - Both `a` and `b` will point to the same object in memory because they are string literals with the same content, and Java reuses strings from the string pool for such literals.

String[] ans = new String[arr.length];

String[] arr = s.split(" ");
String.join(" ",ans);

Integer.parseInt('0');
```

#### Concept 
1.String Pool
It is memory structure inside Heap.
![[Pasted image 20230919081759.png]]

```java
String a = "Kumar";
String b = "Kumar";
//a and b are pointing same object

System.out.println(a); //Kumar
a = "Manglam"; // We are created a new Object and b is pointing to that
System.out.println(b); // Manglam
```

### Why cant we modify Sting Objects
Because If change the string then other references pointing to that object will also get changed.


#### Comparison of Strings
![[Pasted image 20230919084717.png]]


```java
String name1 = new String("Kumar");
String name2 = new String("Kumar");

System.out.println(name1 == name2);
```


#### Benefits using String

```java
sout('a' + 'b'); // 195
sout("a" + "b"); // ab
sout((char)('a' + 3)) // d
sout("a" + 1) // a1 
//integer will converted to Integer and Integer will call .toString()
sout(new Integer(56) + new ArrayList<>()); // It wont work. compile
sout(new Integer(56) + "" new ArrayList<>()); // It will work
// For plus operator atleast one operand should be primitive or string.
operato5 9verloading 
```


The `StringBuilder` class in Java provides a mutable sequence of characters, which is often used for efficiently modifying string data. Here's a list of some of the most commonly used methods available in the `StringBuilder` class:

1. **Constructors**:
    
    - `StringBuilder()`: Constructs a string builder with no characters and an initial capacity of 16 characters.
    - `StringBuilder(CharSequence seq)`: Constructs a string builder initialized to the contents of the specified character sequence.
    - `StringBuilder(int capacity)`: Constructs a string builder with no characters and an initial capacity specified by the `capacity` argument.
    - `StringBuilder(String str)`: Constructs a string builder initialized to the contents of the specified string.
2. **Addition & Insertion**:
    
    - `append(...)`: Overloaded method to append data of different types (like `String`, `CharSequence`, `int`, `char`, etc.) to the end of the current sequence.
    - `insert(int offset, ...)`: Overloaded method to insert data of different types at the specified position.
3. **Deletion & Removal**:
    
    - `delete(int start, int end)`: Removes characters in a substring of this sequence.
    - `deleteCharAt(int index)`: Removes the character at the specified position.
4. **Replacement**:
    
    - `replace(int start, int end, String str)`: Replaces characters in a substring of this sequence with characters in the specified `String`.
5. **Retrieval**:
    
    - `charAt(int index)`: Returns the character at the specified position.
    - `indexOf(String str)`: Returns the index of the first occurrence of the specified substring.
    - `lastIndexOf(String str)`: Returns the index of the last occurrence of the specified substring.
    - `substring(int start)`, `substring(int start, int end)`: Returns a new string that contains a subsequence of characters from the string builder.
    - `length()`: Returns the length (character count).
    - `capacity()`: Returns the current capacity.
6. **Utility**:
    
    - `ensureCapacity(int minimumCapacity)`: Ensures that the capacity is at least equal to the specified minimum.
    - `trimToSize()`: Attempts to reduce storage used for the character sequence.
    - `setLength(int newLength)`: Sets the length of the character sequence.
    - `reverse()`: Reverses the sequence.
7. **Set & Get Methods**:
    
    - `setCharAt(int index, char ch)`: Sets the character at the specified index.
    - `getChars(int srcBegin, int srcEnd, char[] dst, int dstBegin)`: Copies characters from this sequence into the destination character array.
8. **String Representation**:
    
    - `toString()`: Returns a string representing the data in this sequence.




```java
String[] = {'e','s','o','p'}
String ans = String.valueOf(arr);
```

