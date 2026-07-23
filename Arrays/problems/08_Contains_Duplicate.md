# 217. Contains Duplicate

🔗 Problem Link: https://leetcode.com/problems/contains-duplicate/

## Problem Statement

Given an integer array `nums`, return:

- `true` → if any number appears more than once.
- `false` → if all numbers are unique.
## Example 1

Input:

[1,2,3,1]

Output:

true

Explanation:

1 appears two times.

---

## Example 2

Input:

[1,2,3,4]

Output:

false

Explanation:

Every element is unique.

---

## Example 3

Input:

[1,1,1,3,3,4,3,2,4,2]

Output:

true

Explanation:

Many duplicate elements exist.

---

# Approach 1: Using HashSet (Best Approach)

## Idea

A HashSet stores only unique values.

While traversing the array:

- If the element already exists inside the HashSet → duplicate found → return true.
- Otherwise add it to the HashSet.

If the loop finishes, no duplicates exist.

---

## Dry Run

nums = [1,2,3,1]

### Iteration 1

Current number = 1

Set = {}

1 is not present

Add 1

Set = {1}

---

### Iteration 2

Current number = 2

Set = {1}

2 is not present

Add 2

Set = {1,2}

---

### Iteration 3

Current number = 3

Set = {1,2}

3 is not present

Add 3

Set = {1,2,3}

---

### Iteration 4

Current number = 1

Set = {1,2,3}

1 already exists

Return true

---

# Java Code

```java
import java.util.HashSet;

class Solution {

    public boolean containsDuplicate(int[] nums) {

        HashSet<Integer> set = new HashSet<>();

        for(int num : nums){

            if(set.contains(num)){
                return true;
            }

            set.add(num);
        }

        return false;
    }
}
```

# Time Complexity

O(n)

Because we traverse the array only once.

# Space Complexity

O(n)

Because HashSet may store all elements.

---

# Approach 2: Sorting

## Idea

Sort the array first.

If two adjacent elements become equal, duplicate exists.

---

## Java Code

```java
import java.util.Arrays;

class Solution {

    public boolean containsDuplicate(int[] nums) {

        Arrays.sort(nums);

        for(int i=1;i<nums.length;i++){

            if(nums[i]==nums[i-1]){
                return true;
            }

        }

        return false;
    }
}
```

# Time Complexity

O(n log n)

Sorting takes O(n log n)

# Space Complexity

O(1)

(ignoring sorting implementation space)

---

# Which approach should I use?

For interviews:

✅ HashSet approach → Preferred

Because:

- Faster
- Easy to explain
- Most commonly asked

---

# Key Learning

Whenever you see:

"Check if duplicates exist"

Think:

👉 HashSet

HashSet = Fast searching + Unique elements
