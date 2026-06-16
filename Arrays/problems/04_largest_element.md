# Largest Element in the Array

## Learning Sources

GeeksforGeeks: https://www.geeksforgeeks.org/java-program-to-find-largest-element-in-an-array/

## Problem Statement

Given an array of integers, find the largest element present in the array.

## Example

Input:

[10, 25, 5, 80, 40]

Output:

80

## Concept Used

* Array Traversal
* Comparison
* Updating Maximum Value

## My Understanding

We start by assuming the first element is the largest. Then we traverse the array and compare every element with the current largest value. If we find a bigger number, we update the largest value.

## My Approach

1. Create an array.
2. Assume first element is the largest.
3. Traverse from index 1.
4. Compare each element with current largest.
5. If bigger, update largest.
6. Print the largest value.

## Algorithm

1. Set `max = arr[0]`.
2. Traverse array from index `1`.
3. If `arr[i] > max`, update `max`.
4. Print or return `max`.

## Code in Java

```java
public class LargestElement {

    public static int findLargest(int[] arr) {

        int max = arr[0];

        for(int i=1;i<arr.length;i++){

            if(arr[i] > max){
                max = arr[i];
            }

        }

        return max;
    }

    public static void main(String[] args) {

        int[] arr = {10,25,5,80,40};

        System.out.println(findLargest(arr));
    }
}
```

## Time Complexity

*O(n)*

Reason: We traverse the array once.

## Space Complexity

*O(1)*

Reason: Only one variable `max` is used.

## Important Points

* Initialize `max` with first element.
* Do not initialize `max = 0` because arrays can contain negative numbers.
* Traverse from index `1`.

## What I Learned

* How to track a maximum value.
* Why `arr[0]` is safer than `0`.
* How linear traversal works.

**Pro tip:** Interviewers may ask how to find largest without sorting because sorting takes `O(n log n)` while this takes `O(n)`.
