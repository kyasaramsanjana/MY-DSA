# Sum of Array Elements

## Learning Sources

GeeksforGeeks: https://www.geeksforgeeks.org/sum-elements-array/

## Problem Statement

Given an array of integers, find the sum of all elements present in the array.

Return the total sum.

## Example

Input:

[10, 20, 30, 40, 50]

Output:

150

---

## Concept Used

- Array Traversal
- Accumulator Variable

---

## My Understanding

To find the sum of an array, we traverse each element and continuously add it to a variable called `sum`.

After reaching the end of the array, `sum` contains the final answer.

---

## My Approach

1. Create a variable `sum = 0`.
2. Traverse the entire array.
3. Add each element to `sum`.
4. Return or print `sum`.

---

## Algorithm

1. Initialize `sum = 0`.
2. Traverse array from index 0.
3. Add current element to `sum`.
4. Continue until the end.
5. Return `sum`.

---

## Code in Java

```java
public class SumOfArray {

    public static int findSum(int[] arr) {

        int sum = 0;

        for(int i = 0; i < arr.length; i++) {

            sum += arr[i];

        }

        return sum;
    }

    public static void main(String[] args) {

        int[] arr = {10, 20, 30, 40, 50};

        System.out.println(findSum(arr));

    }
}
```

## Output

```text
150
```

---

## Time Complexity

*O(n)*

Reason: We traverse the array once.

---

## Space Complexity

*O(1)*

Reason: Only one extra variable `sum` is used.

---

## Important Points

- Initialize `sum` to 0.
- Every element contributes once.
- Empty array returns 0.
- Negative numbers also work correctly.

---

## What I Learned

- How array traversal works.
- How accumulator variables work.
- How to process all elements efficiently.

**Pro tip:** Interviewers may ask average after this.

Formula:

```java
average = sum / arr.length;
```
