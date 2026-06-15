# Reverse the Array

## Learning Sources
* GeeksforGeeks: https://www.geeksforgeeks.org/write-a-program-to-reverse-an-array-or-string/

## Problem Statement
Given an array of integers, reverse the array in-place. Return the reversed array.

### Example
Input:
```text
[10, 20, 30, 40, 50]

Output:
[50, 40, 30, 20, 10]


## Concept Used
- Array Traversal
- Two Pointers
- Swapping

## My Understanding
To reverse, we need to swap the first element with last, second with second-last, and so on. We stop when we reach the middle. No need to use extra array if we do it in-place.

## My Approach
1. Create an array.
2. Take two pointers: `start = 0`, `end = arr.length - 1`.
3. While `start < end`, swap `arr[start]` and `arr[end]`.
4. Increment `start`, decrement `end`.
5. Stop when `start >= end`.

## Algorithm
1. Initialize `start = 0`, `end = arr.length - 1`.
2. While `start < end`:
   a. Swap `arr[start]` and `arr[end]`.
   b. `start++`, `end--`.
3. Print or return the array.

## Code in Java
import java.util.Arrays;

public class ReverseArray {
    public static void reverse(int[] arr) {
        int start = 0;
        int end = arr.length - 1;
        
        while (start < end) {
            // Swap arr[start] and arr[end]
            int temp = arr[start];
            arr[start] = arr[end];
            arr[end] = temp;
            
            start++;
            end--;
        }
    }

    public static void main(String[] args) {
        int[] arr = {10, 20, 30, 40, 50};
        System.out.println("Original: " + Arrays.toString(arr));
        
        reverse(arr);
        
        System.out.println("Reversed: " + Arrays.toString(arr));
    }
}


## Time Complexity
*O(n)*
Reason: Each element is swapped once. Total `n/2` swaps, so linear time.

## Space Complexity
*O(1)*
Reason: In-place reversal. Only 2 pointer variables used. No extra array.

## Important Points
- Use `start < end` not `start <= end`. If equal, it's the middle element, no swap needed.
- For in-place, swap using temp variable or XOR trick.
- If you create a new array and copy backwards, space becomes *O(n)*.
- Empty array and single element array are already reversed.

## What I Learned
- How two pointer technique works.
- In-place vs extra space trade-off.
- Why loop condition `start < end` prevents re-swapping middle elements.
- How to swap using temp variable in Java.

**Pro tip:** If interviewer asks, also mention recursive way:
```java
reverse(arr, start+1, end-1) 
