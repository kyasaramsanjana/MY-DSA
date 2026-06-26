# 876. Middle of the Linked List

## 1. Understand the problem

We are given:

* `head` → starting node of a linked list.

We must **return the middle node**.

If there are **2 middle nodes**, return the **second middle node**.

---

## Example 1

Input

```text
head = [1,2,3,4,5]
```

Linked List

```text
1 → 2 → 3 → 4 → 5 → null
```

Output

```text
3 → 4 → 5 → null
```

Middle = 3

---

## Example 2

Input

```text
head = [1,2,3,4,5,6]
```

Linked List

```text
1 → 2 → 3 → 4 → 5 → 6 → null
```

There are two middle nodes:

```text
3 and 4
```

Return the second one.

Output

```text
4 → 5 → 6 → null
```

---

# 2. Observation

A simple approach:

1. Count total nodes.
2. Divide by 2.
3. Traverse again.

This needs **2 traversals**.

We can do better.

---

# 3. Best approach (Slow and Fast pointers)

Use two pointers.

```text
slow
fast
```

Rules:

```text
slow = move 1 step

fast = move 2 steps
```

When fast reaches the end,

```text
slow will be at the middle
```

---

# 4. Initial setup

```text
slow = head

fast = head
```

Picture

```text
1 → 2 → 3 → 4 → 5

↑
slow

↑
fast
```

---

# 5. Move them

Loop:

```java
while(fast != null && fast.next != null)
```

Inside loop:

```java
slow = slow.next;

fast = fast.next.next;
```

---

# 6. Dry Run

Input

```text
1 → 2 → 3 → 4 → 5
```

Initially

```text
slow = 1

fast = 1
```

### First iteration

```text
slow = 2

fast = 3
```

Picture

```text
1 → 2 → 3 → 4 → 5

    ↑

   slow

        ↑

       fast
```

---

### Second iteration

```text
slow = 3

fast = 5
```

Picture

```text
1 → 2 → 3 → 4 → 5

        ↑

       slow

                ↑

               fast
```

---

### Third iteration

Fast cannot move.

Loop stops.

Return

```text
slow
```

Answer

```text
3 → 4 → 5
```

---

# 7. Dry Run (Even length)

Input

```text
1 → 2 → 3 → 4 → 5 → 6
```

Initially

```text
slow = 1

fast = 1
```

### Iteration 1

```text
slow = 2

fast = 3
```

### Iteration 2

```text
slow = 3

fast = 5
```

### Iteration 3

```text
slow = 4

fast = null
```

Stop.

Answer

```text
4 → 5 → 6
```

It automatically gives the **second middle node**.

---

# 8. Algorithm

1. Create two pointers.

```text
slow = head

fast = head
```

2. While fast and fast.next exist

```text
move slow by 1 step

move fast by 2 steps
```

3. Return slow.

---

# 9. Java Code

```java
class Solution {

    public ListNode middleNode(ListNode head) {

        ListNode slow = head;

        ListNode fast = head;

        while (fast != null && fast.next != null) {

            slow = slow.next;

            fast = fast.next.next;
        }

        return slow;
    }
}
```

# 10. Time Complexity

```text
O(n)
```

We traverse the list once.

---

# 11. Space Complexity

```text
O(1)
```

Only two pointers are used.

---

# 12. One-line note for interviews

> **If you need the middle of a linked list, use Slow and Fast pointers. Slow moves 1 step, Fast moves 2 steps. When Fast reaches the end, Slow reaches the middle.** 🚀
