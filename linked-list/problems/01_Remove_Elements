# 203. Remove Linked List Elements

## 1. Understand the problem

We are given:

* `head` → starting node of a linked list
* `val` → a value to remove

We must **delete every node whose value = val**.

Return the new head.

---

## Example

Input:

```
head = [1,2,6,3,4,5,6]

val = 6
```

### Before

```
head

 ↓

1 → 2 → 6 → 3 → 4 → 5 → 6 → null
```

Remove all `6`.

### After

```
1 → 2 → 3 → 4 → 5 → null
```

---

# Important observation

What if the first node itself has to be removed?

Example:

```
7 → 7 → 7 → null

val = 7
```

If we remove the first node, `head` changes.

That's why handling the head separately becomes difficult.

So we use a **dummy node**.

---

# 2. Dummy node concept

Create an extra node before head.

```
dummy → 1 → 2 → 6 → 3 → 4 → 5 → 6 → null
```

```
dummy = extra helper node

dummy.next = head
```

Now even if the first node is deleted, we can easily connect nodes.

---

# 3. Idea

We only need one pointer.

```
current = dummy
```

At every step, check:

```
current.next
```

Why?

Because to delete a node, we need access to its previous node.

---

## Case 1: Found value

Suppose

```
dummy → 1 → 2 → 6 → 3
                 ↑
          current.next
```

`6 == val`

Delete it:

```
current.next = current.next.next
```

Picture:

Before

```
2 → 6 → 3
```

After

```
2 → 3
```

---

## Case 2: Not equal

Move forward.

```
current = current.next
```

---

# 4. Algorithm

1. Create dummy node.
2. Connect dummy to head.
3. Start current from dummy.
4. Traverse until `current.next != null`.
5. If value matches → delete.
6. Else → move current.
7. Return `dummy.next`.

---

# 5. Dry run

Input

```
1 → 2 → 6 → 3 → 4 → 5 → 6

val = 6
```

Initially

```
dummy → 1 → 2 → 6 → 3 → 4 → 5 → 6
```

`current = dummy`

### Step 1

```
current.next = 1
```

Not 6.

Move.

### Step 2

```
current.next = 2
```

Not 6.

Move.

### Step 3

```
current.next = 6
```

Delete.

```
2 → 3
```

List becomes

```
dummy → 1 → 2 → 3 → 4 → 5 → 6
```

Continue.

### Last 6

Delete again.

Final

```
1 → 2 → 3 → 4 → 5
```

---

# 6. Java code

```java
class Solution {

    public ListNode removeElements(ListNode head, int val) {

        ListNode dummy = new ListNode(0);

        dummy.next = head;

        ListNode current = dummy;

        while (current.next != null) {

            if (current.next.val == val) {

                current.next = current.next.next;

            } else {

                current = current.next;
            }
        }

        return dummy.next;
    }
}
```

# 7. Time Complexity

```
O(n)
```

We visit each node once.

# 8. Space Complexity

```
O(1)
```

Only extra pointers are used.

---

📌 **One-line note to remember for interviews**

> **To delete a node in a linked list, always keep access to the previous node. Dummy nodes make head deletion easy.**
