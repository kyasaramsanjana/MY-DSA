
LeetCode:https://leetcode.com/problems/missing-number/
Problem Statement

Given an array nums containing n distinct numbers in the range [0, n], return the only number that is missing from the array.

Example 1

Input:

[3, 0, 1]

Output:
2
Example 2

Input:

[0, 1]

Output:
2
Example 3

Input:

[9,6,4,2,3,5,7,0,1]

Output:
8
Concept Used
Sum Formula
Array Traversal
Mathematics
My Understanding

The array contains numbers from 0 to n, but one number is missing.

We know the sum of numbers from 0 to n can be found using:

2
n(n+1)
	​


If we calculate the expected sum and subtract the actual array sum, the remaining value is the missing number.

My Approach
Find n = nums.length.
Calculate expected sum using n*(n+1)/2.
Traverse the array and calculate actual sum.
Subtract actual sum from expected sum.
Return the answer.
Algorithm
Store n = nums.length.
Calculate expectedSum = n*(n+1)/2.
Initialize actualSum = 0.
Traverse the array and add all elements to actualSum.
Return expectedSum - actualSum.
Java Code
class Solution {
    public int missingNumber(int[] nums) {

        int n = nums.length;

        int expectedSum = n * (n + 1) / 2;

        int actualSum = 0;

        for (int num : nums) {
            actualSum += num;
        }

        return expectedSum - actualSum;
    }
}
Time Complexity

O(n)

Reason: We traverse the array only once.

Space Complexity

O(1)

Reason: Only a few extra variables are used.

Important Points
Array contains numbers from 0 to n.
Exactly one number is missing.
Numbers are unique (no duplicates).
The formula n*(n+1)/2 helps avoid sorting.
This is more efficient than sorting.
Alternative Approach (XOR)

We can also use XOR.

class Solution {
    public int missingNumber(int[] nums) {

        int xor = nums.length;

        for (int i = 0; i < nums.length; i++) {
            xor ^= i;
            xor ^= nums[i];
        }

        return xor;
    }
}
XOR Complexity
Time Complexity: O(n)
Space Complexity: O(1)
What I Learned
How to use mathematical formulas to optimize problems.
How to avoid sorting and extra space.
How XOR can cancel equal numbers.
Multiple ways can solve the same problem efficiently.
