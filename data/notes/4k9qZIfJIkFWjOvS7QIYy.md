
An array is a (usually) fixed-length data structure that stores one type of element in order. Read/write times are always `O(1)` however resizing is `O(n)`.

```Java
var myArray = new int[10];
myArray[2]; // O(1)
myArray[2] = 13; // O(1)
// To resize an array...
Arrays.copyOf(myArray, myArray.length * 2); // O(n)
```