Topic: Arrays
Learning Sources

GeeksforGeeks:https://www.geeksforgeeks.org/java/arrays-in-java/

Arrays in Java - GeeksforGeeks

What is an Array?

An array is a data structure used to store multiple values of the same data type in a single variable.

All elements are stored in contiguous (continuous) memory locations.

Example
int[] arr = {10,20,30,40,50};
✅_____Why do we use Arrays?
To store multiple values in one variable.
Easy access using indexes.
Easy traversal using loops.
Better organization of data.
✅_____Characteristics of Arrays
Fixed size.
Stores only similar data types.
Indexing starts from 0.
Stored in contiguous memory.
✅_____Important Terms

1. Index

The position of an element inside an array.

arr[0] = 10
arr[1] = 20
arr[2] = 30
2. Length

The total number of elements inside an array.

arr.length
✅ Array Traversal

Visiting every element one by one.

for(int i=0;i<arr.length;i++){
   System.out.println(arr[i]);
}
✅ Common Operations
Traversal
Searching
Insertion
Deletion
Updating
⏱️ Time Complexities
Operation	Complexity
Access	O(1)
Traversal	O(n)
Search	O(n)
Insertion	O(n)
Deletion	O(n)
❌ Common Mistakes
Using i <= arr.length
Accessing invalid indexes
Forgetting indexing starts from 0
📝 What I Learned Today

✔ Arrays store multiple values.

✔ Arrays store the same data type.

✔ Indexing starts from 0.

✔ arr.length gives the size.

✔ Traversal uses loops.

✔ Arrays have fixed size.
