# Arrays

## Learning Sources

* GeeksforGeeks: https://www.geeksforgeeks.org/arrays-in-java/
* YouTube: (Paste the video link you learned from)

## What is an Array?

An array is a collection of elements of the same data type stored in contiguous memory locations.

Example:

```java
int[] arr = {10, 20, 30, 40, 50};
```

## Why Do We Use Arrays?

* Store multiple values in a single variable.
* Easy access using indexes.
* Efficient traversal using loops.

## Array Characteristics

* Fixed size.
* Stores similar data types.
* Indexing starts from 0.
* Stored in contiguous memory.

## Important Terms

### Index

Position of an element in the array.

Example:

```java
arr[0] = 10
arr[1] = 20
arr[2] = 30
```

### Length

Number of elements in the array.

```java
arr.length
```

## Array Traversal

Visiting every element of an array one by one.

```java
for(int i = 0; i < arr.length; i++) {
    System.out.println(arr[i]);
}
```

## Common Operations

1. Traversal
2. Searching
3. Insertion
4. Deletion
5. Updating

## Time Complexities

| Operation | Time Complexity |
| --------- | --------------- |
| Access    | O(1)            |
| Traversal | O(n)            |
| Search    | O(n)            |
| Insertion | O(n)            |
| Deletion  | O(n)            |

## Common Mistakes

* Using `i <= arr.length`
* Accessing invalid indexes
* Forgetting array indexing starts from 0

## What I Learned

* Arrays store multiple values.
* Array indexing starts from 0.
* Traversal uses loops.
* `arr.length` gives the size of the array.
* Arrays have fixed size.
