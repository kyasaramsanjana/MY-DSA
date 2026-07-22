# 📚 Queue Notes (Complete DSA Notes)

---

# Queue

A **Queue** is a **Linear Data Structure** that follows the **FIFO (First In First Out)** principle.

👉 The element that is inserted first is removed first.

### Real Life Examples

* People standing in a ticket counter.
* Printer queue.
* CPU Scheduling.
* Call Center.
* Food delivery orders.

---

# FIFO (First In First Out)

Imagine 5 people standing in a line.

```
Front                         Rear

[A] [B] [C] [D] [E]
```

* A entered first.
* B entered second.
* E entered last.

Now if someone leaves...

```
A leaves first
```

Then

```
Front                    Rear

[B] [C] [D] [E]
```

Again

```
B leaves
```

Queue always removes from the **Front**.

New people always join at the **Rear**.

---

# Queue Operations

There are mainly **6 operations**.

| Operation    | Meaning              |
| ------------ | -------------------- |
| Enqueue      | Insert element       |
| Dequeue      | Remove element       |
| Front / Peek | Return first element |
| Rear         | Return last element  |
| isEmpty      | Check queue is empty |
| Size         | Number of elements   |

---

# Queue Representation

```
Front                      Rear

10 → 20 → 30 → 40
```

Front = 10

Rear = 40

---

# Enqueue

Insert an element at the **Rear**.

Before

```
Front             Rear

10 → 20 → 30
```

Insert 40

After

```
Front                  Rear

10 → 20 → 30 → 40
```

Time Complexity

```
O(1)
```

---

# Dequeue

Remove element from the **Front**.

Before

```
Front                  Rear

10 → 20 → 30 → 40
```

Remove

```
10
```

After

```
Front             Rear

20 → 30 → 40
```

Time Complexity

```
O(1)
```

---

# Peek / Front

Returns the first element.

Queue

```
Front

10 → 20 → 30
```

Answer

```
10
```

No deletion happens.

Time Complexity

```
O(1)
```

---

# Rear

Returns last element.

Queue

```
10 → 20 → 30

             Rear
```

Answer

```
30
```

Time Complexity

```
O(1)
```

---

# isEmpty()

Checks if queue contains elements.

Queue

```
[]
```

Returns

```
true
```

Queue

```
10 20
```

Returns

```
false
```

---

# Size()

Returns number of elements.

Queue

```
10 20 30 40
```

Size

```
4
```

---

# Queue Example

Operations

```
Enqueue(10)

Queue

10
```

---

```
Enqueue(20)

Queue

10 20
```

---

```
Enqueue(30)

Queue

10 20 30
```

---

```
Dequeue()

Removed

10

Queue

20 30
```

---

```
Enqueue(40)

Queue

20 30 40
```

---

```
Front()

20
```

---

```
Rear()

40
```

---

# Queue using Array

```
Index

0   1   2   3   4

10 20 30 40
```

We maintain

```
Front Index

Rear Index
```

Example

```
Front = 0

Rear = 3
```

---

## Enqueue

```
rear++

arr[rear] = value
```

---

## Dequeue

```
front++
```

No shifting required.

---

### Problem in Simple Queue

Suppose array size = 5

```
0 1 2 3 4

10 20 30 40 50
```

Front = 0

Rear = 4

Now dequeue three times.

```
_ _ _ 40 50
```

Front = 3

Rear = 4

Now enqueue(60)

Cannot insert!

Even though first three spaces are empty.

This is called

```
False Overflow
```

To solve this,

We use

```
Circular Queue
```

---

# Queue using Linked List

Each node has

```
Data

Next Pointer
```

Maintain

```
Front Pointer

Rear Pointer
```

Example

```
Front

10 → 20 → 30 → NULL

               Rear
```

Enqueue

```
Attach new node at Rear.
```

Dequeue

```
Move Front to next node.
```

Advantages

* Dynamic size
* No overflow until memory ends
* O(1) enqueue
* O(1) dequeue

---

# Types of Queue

1. Simple Queue
2. Circular Queue
3. Deque (Double Ended Queue)
4. Priority Queue

Let's understand each one.

---

# 1. Simple Queue

Insertion

```
Rear
```

Deletion

```
Front
```

```
Front                  Rear

10 → 20 → 30
```

---

# 2. Circular Queue

Last position connects to first.

Instead of wasting space,

```
Rear wraps around.
```

Example

```
0 1 2 3 4

10 20 30 _ _
```

After deletions

```
_ _ 30 _ _
```

Instead of saying array is full,

Rear comes back.

```
60 goes to index 0

70 goes to index 1
```

Visualization

```
     0
   /   \
4       1
|       |
3       2
```

Time Complexity

```
Enqueue O(1)

Dequeue O(1)
```

---

# 3. Deque

Double Ended Queue.

Insertion from

* Front
* Rear

Deletion from

* Front
* Rear

Example

```
Front

10 20 30

Rear
```

Can insert

```
5
```

at front.

Can insert

```
40
```

at rear.

Can remove from both ends.

---

Types

### Input Restricted Deque

Insert only from Rear.

Delete from both.

---

### Output Restricted Deque

Delete only from Front.

Insert from both.

---

# 4. Priority Queue

Removal depends on

```
Priority
```

Not FIFO.

Example

```
Patient Queue

Critical Patient

Normal Patient
```

Critical patient treated first.

Example

```
(5,A)

(1,B)

(3,C)
```

Priority

```
1 highest
```

Output

```
B

C

A
```

---

# Time Complexities

| Operation | Array | Linked List |
| --------- | ----- | ----------- |
| Enqueue   | O(1)  | O(1)        |
| Dequeue   | O(1)* | O(1)        |
| Front     | O(1)  | O(1)        |
| Rear      | O(1)  | O(1)        |
| isEmpty   | O(1)  | O(1)        |
| Size      | O(1)  | O(1)        |

*Assuming we use front and rear indices (no shifting).

---

# Applications of Queue

* CPU Scheduling
* Printer Queue
* BFS (Breadth First Search)
* Level Order Traversal in Trees
* Network Packet Scheduling
* Call Center Systems
* Ticket Booking Systems
* Order Processing Systems
* Keyboard Buffer
* Message Queues
* Multiplayer Game Event Processing

---

# Queue vs Stack

| Stack             | Queue                      |
| ----------------- | -------------------------- |
| LIFO              | FIFO                       |
| Insert at Top     | Insert at Rear             |
| Delete from Top   | Delete from Front          |
| One pointer (Top) | Two pointers (Front, Rear) |
| Example: Plates   | Example: Waiting line      |

---

# Important Interview Questions

### Easy

* 232. Implement Queue using Stacks
* 225. Implement Stack using Queues
* 933. Number of Recent Calls
* 346. Moving Average from Data Stream

### Medium

* 622. Design Circular Queue
* 641. Design Circular Deque
* 649. Dota2 Senate
* 2073. Time Needed to Buy Tickets
* 1700. Number of Students Unable to Eat Lunch

### Hard

* 239. Sliding Window Maximum (Deque)
* 862. Shortest Subarray with Sum at Least K (Monotonic Queue)

---

# Key Points to Remember

* Queue follows **FIFO (First In, First Out)**.
* **Enqueue** inserts at the **rear**.
* **Dequeue** removes from the **front**.
* Two pointers are commonly used: **front** and **rear**.
* A simple array queue can suffer from **false overflow**; a **circular queue** fixes this by reusing freed spaces.
* **Deque** allows insertion and deletion at both ends.
* **Priority Queue** removes elements based on priority rather than insertion order.
* Queues are heavily used in **BFS**, **scheduling**, **buffering**, **networking**, and **real-time systems**.

These notes provide a solid foundation before you start solving queue problems like **933 → 346 → 225 → 649 → 622 → 641 → 239**.
