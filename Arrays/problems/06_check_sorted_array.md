# Check if Array is Sorted

## Learning Sources

GeeksforGeeks: https://www.geeksforgeeks.org/check-if-an-array-is-sorted/

## Problem Statement

Given an array of integers, check whether the array is sorted in ascending order or not.

If every element is smaller than or equal to the next element, the array is sorted.

Return `true` if sorted, otherwise return `false`.

## Example

Input:

[10, 20, 30, 40, 50]

Output:

true

Another Example

Input:

[10, 30, 20, 40, 50]

Output:

false

---

## Concept Used

- Array Traversal
- Adjacent Element Comparison
- Boolean Flag

---

## My Understanding

To check if an array is sorted, we compare every element with its next element.

If we find any element greater than the next element, the array is not sorted.

If we reach the end without finding any violation, the array is sorted.

---

## My Approach

1. Traverse the array from index 0.
2. Compare `arr[i]` with `arr[i+1]`.
3. If `arr[i] > arr[i+1]`, return false.
4. If the loop finishes, return true.

---

## Algorithm

1. Start loop from `i = 0`.
2. Run until `arr.length - 1`.
3. Compare current element with next element.
4. If current element is greater, return false.
5. Otherwise continue.
6. Return true.

---

## Code in Java

```java
public class CheckSortedArray {

    public static boolean isSorted(int[] arr) {

        for(int i = 0; i < arr.length - 1; i++) {

            if(arr[i] > arr[i + 1]) {
                return false;
            }

        }

        return true;
    }

    public static void main(String[] args) {

        int[] arr = {10, 20, 30, 40, 50};

        System.out.println(isSorted(arr));

    }
}
```

## Output

```text
true
```

---

## Time Complexity

*O(n)*

Reason: We traverse the array only once.

---

## Space Complexity

*O(1)*

Reason: No extra data structure is used.

---

## Important Points

- Use `arr.length - 1` because we compare with `i + 1`.
- If any element is greater than the next element, the array is not sorted.
- Empty array is considered sorted.
- Single element array is also considered sorted.
- This logic checks ascending order only.

---

## What I Learned

- How to traverse arrays efficiently.
- How adjacent element comparison works.
- How to use boolean return values.
- Why we stop at `arr.length - 1`.
- How to identify sorted arrays quickly.
