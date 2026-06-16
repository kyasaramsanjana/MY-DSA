# Second Largest Element in the Array

## Learning Sources

GeeksforGeeks: https://www.geeksforgeeks.org/find-second-largest-element-array/

## Problem Statement

Given an array of integers, find the second largest element.

## Example

Input:

[10, 25, 5, 80, 40]

Output:

40

## Concept Used

* Array Traversal
* Comparison
* Maximum Tracking

## My Understanding

We need two variables:

* `largest`
* `secondLargest`

While traversing the array, update both whenever necessary.

## My Approach

1. Create two variables.
2. Set both to smallest possible integer.
3. Traverse the array.
4. If current element is larger than largest:

   * Move largest to secondLargest.
   * Update largest.
5. Else if current element is bigger than secondLargest and not equal to largest:

   * Update secondLargest.
6. Return secondLargest.

## Algorithm

1. Initialize `largest` and `secondLargest`.
2. Traverse array.
3. Update values accordingly.
4. Return secondLargest.

## Code in Java

```java
public class SecondLargest {

    public static int findSecondLargest(int[] arr){

        int largest = Integer.MIN_VALUE;
        int secondLargest = Integer.MIN_VALUE;

        for(int num : arr){

            if(num > largest){

                secondLargest = largest;
                largest = num;

            }

            else if(num > secondLargest && num != largest){

                secondLargest = num;

            }

        }

        return secondLargest;
    }

    public static void main(String[] args){

        int[] arr = {10,25,5,80,40};

        System.out.println(findSecondLargest(arr));

    }

}
```

## Time Complexity

*O(n)*

Reason: Single traversal.

## Space Complexity

*O(1)*

Reason: Only two variables are used.

## Important Points

* Use `Integer.MIN_VALUE`.
* Handle duplicate largest values.
* Do not sort the array because sorting takes `O(n log n)`.

## What I Learned

* How to track two values simultaneously.
* How to avoid duplicates.
* How to solve efficiently in one pass.

**Pro tip:** If all elements are same, second largest does not exist.
