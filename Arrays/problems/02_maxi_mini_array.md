 Find Maximum and Minimum in Array

## Learning Sources
* GeeksforGeeks: https://www.geeksforgeeks.org/program-to-find-largest-element-in-an-array/
## Problem Statement
Given an array of integers, find the maximum and minimum element in the array.
### Example
Input:
```text
[10, 20, 5, 40, 30]

Output:
Maximum = 40
Minimum = 5


## Concept Used
* Array Traversal
* Comparison
* Single Loop

## My Understanding
To find max and min, we have to check every element once. We can keep two variables `max` and `min` initialized with first element. Then compare each element: if bigger than `max`, update `max`. If smaller than `min`, update `min`.

## My Approach
1. Create an array.
2. Initialize `max = arr[0]` and `min = arr[0]`.
3. Start loop from index 1 to last index.
4. If `arr[i] > max`, update `max`.
5. If `arr[i] < min`, update `min`.
6. Print `max` and `min`.

## Algorithm
1. Initialize `max = arr[0]`, `min = arr[0]`.
2. Run a loop from `i = 1` to `i < arr.length`.
3. If `arr[i] > max`, set `max = arr[i]`.
4. If `arr[i] < min`, set `min = arr[i]`.
5. Print `max` and `min`.

## Time Complexity
*O(n)*
Reason: We traverse the array only once. Every element is compared once.

## Space Complexity
*O(1)*
Reason: Only two extra variables `max` and `min` used. No extra array.

## Important Points
* Initialize both `max` and `min` with `arr[0]`, not 0. If array has all negative numbers, initializing with 0 breaks logic.
* Start loop from `i = 1` since `arr[0]` is already considered.
* For empty array edge case, handle separately or throw error.
* Can also be done using `Arrays.stream(arr).max()` and `min()` in Java, but manual loop builds logic.

## What I Learned
* How to track running maximum and minimum in one pass.
* Why initialization matters for negative numbers.
* How to reduce two loops to a single loop for efficiency.
* Edge case handling for empty arrays.
