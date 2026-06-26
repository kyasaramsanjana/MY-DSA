# Printing the Array

## Learning Sources

* GeeksforGeeks: https://www.geeksforgeeks.org/arrays-in-java/

## Problem Statement

Given an array of integers, print all elements of the array.

### Example

Input:

```text
[10, 20, 30, 40, 50]
```

Output:

```text
10 20 30 40 50
```

## Concept Used

* Array Traversal
* For Loop

## My Understanding

An array is a collection of elements stored in contiguous memory locations. To print all elements, we need to visit each index one by one.

## My Approach

1. Create an array.
2. Start a loop from index 0.
3. Continue until the last index.
4. Print the element at the current index.

## Algorithm

1. Initialize an array.
2. Run a loop from `i = 0` to `i < arr.length`.
3. Print `arr[i]`.

## Time Complexity

**O(n)**

Reason: Every element is visited exactly once.

## Space Complexity

**O(1)**

Reason: No extra space is used.

## Important Points

* Array indexing starts from 0.
* Last index = `arr.length - 1`.
* `arr.length` gives the size of the array.
* Using `i <= arr.length` causes `ArrayIndexOutOfBoundsException`.

## What I Learned

* How to traverse an array.
* How to access elements using indexes.
* How to use `arr.length`.
* Why loop conditions are important.
